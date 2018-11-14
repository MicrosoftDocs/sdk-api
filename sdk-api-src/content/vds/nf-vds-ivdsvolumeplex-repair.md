---
UID: NF:vds.IVdsVolumePlex.Repair
title: IVdsVolumePlex::Repair
author: windows-sdk-content
description: Repairs a fault-tolerant volume plex by moving bad members to good disks.
old-location: base\ivdsvolumeplex_repair.htm
tech.root: VDS
ms.assetid: 21c91e85-8a49-4e74-9191-37aeb03b299e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsVolumePlex interface [VDS],Repair method, IVdsVolumePlex.Repair, IVdsVolumePlex::Repair, Repair, Repair method [VDS], Repair method [VDS],IVdsVolumePlex interface, base.ivdsvolumeplex_repair, vds/IVdsVolumePlex::Repair
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVolumePlex.Repair
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vds.h
: 
- IVdsVolumePlex.Repair
: 
---

# IVdsVolumePlex::Repair


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Repairs a fault-tolerant 
   volume plex by moving bad members to good disks.


## -parameters




### -param pInputDiskArray [in]

Pointer to an array of <a href="https://msdn.microsoft.com/837981e5-8600-4add-85cf-a802615133d3">VDS_INPUT_DISK</a> structures, 
      one structure for each disk.
      

<div class="alert"><b>Note</b>  Include only the required members of this structure (<b>diskId</b> and 
       <b>ullSize</b>).</div>
<div> </div>
<b>Windows Server 2003:  </b>only volumes that are striped with parity (RAID-5) can be repaired with this method, and only one new disk can 
        be passed to this method at a time.


### -param lNumberOfDisks [in]

The total number of disks in the volume.


### -param ppAsync [out]

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer, which VDS 
      initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or query the 
      status of the operation.

If you call <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> on this method and a success HRESULT value is returned, you 
      must release the interfaces returned in the 
      <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="https://msdn.microsoft.com/en-us/library/ms687197(v=VS.85).aspx">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/en-us/library/ms693474(v=VS.85).aspx">FAILED</a> macros defined in Winerror.h.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The repair completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The caller attempted to repair the plex of a basic volume, which is always healthy and never needs repair.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_REPAIR_VOLUMESTATE</b></dt>
<dt>0x80042460L</dt>
</dl>
</td>
<td width="60%">
The plex or volume is not accessible. In addition, this error can be returned when the status of a plex is 
        not one of the following: failing redundancy, failed redundancy, or failed redundancy failing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_IN_USE_BY_VOLUME</b></dt>
<dt>0x8004244CL</dt>
</dl>
</td>
<td width="60%">
One or more extents of the disk are already being used by the volume.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_INCOMPLETE</b></dt>
<dt>0x80042432L</dt>
</dl>
</td>
<td width="60%">
The volume is missing one or more members or is somehow incomplete.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a>



<a href="https://msdn.microsoft.com/91970f8b-2b19-4054-8aa2-28e1ea74b3f6">IVdsVolumePlex</a>



<a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a>



<a href="https://msdn.microsoft.com/837981e5-8600-4add-85cf-a802615133d3">VDS_INPUT_DISK</a>
 

 

