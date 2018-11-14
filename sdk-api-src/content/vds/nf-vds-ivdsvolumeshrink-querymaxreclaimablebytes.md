---
UID: NF:vds.IVdsVolumeShrink.QueryMaxReclaimableBytes
title: IVdsVolumeShrink::QueryMaxReclaimableBytes
author: windows-sdk-content
description: Retrieves the maximum number of bytes that can be reclaimed from the current volume.
old-location: base\ivdsvolumeshrink_querymaxreclaimablebytes.htm
tech.root: VDS
ms.assetid: 416ceb78-50fb-4976-8814-3981b594ebec
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsVolumeShrink interface,QueryMaxReclaimableBytes method, IVdsVolumeShrink.QueryMaxReclaimableBytes, IVdsVolumeShrink::QueryMaxReclaimableBytes, QueryMaxReclaimableBytes, QueryMaxReclaimableBytes method, QueryMaxReclaimableBytes method,IVdsVolumeShrink interface, base.ivdsvolumeshrink_querymaxreclaimablebytes, vds/IVdsVolumeShrink::QueryMaxReclaimableBytes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVdsVolumeShrink.QueryMaxReclaimableBytes
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
- IVdsVolumeShrink.QueryMaxReclaimableBytes
: 
---

# IVdsVolumeShrink::QueryMaxReclaimableBytes


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Retrieves the maximum number of bytes that can be reclaimed from the current volume.


## -parameters




### -param pullMaxNumberOfReclaimableBytes [out]

Pointer to a variable that upon successful completion receives the maximum number of bytes which can be reclaimed from the current volume.  This number will always be a multiple of the file system cluster size, which is in turn a multiple of the disk sector size. This parameter is required and cannot be null.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANNOT_SHRINK</b></dt>
<dt>0x8004251EL</dt>
</dl>
</td>
<td width="60%">
The volume cannot be shrunk because the file system does not support it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_REMOVEABLE</b></dt>
<dt>0x8004255AL</dt>
</dl>
</td>
<td width="60%">
The operation is not supported on removable media.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPX_X_NULL_REF_POINTER</b></dt>
<dt>0x800706F4</dt>
</dl>
</td>
<td width="60%">
The <i>pullMaxNumberOfReclaimableBytes</i> parameter was null on input.

</td>
</tr>
</table>
 




## -remarks



This method can return more reclaimable bytes than are actually available. For more information, see "IVdsVolumeShrink::Shrink fails when provided value returned from QueryMaxReclaimableBytes" in the Help and Support Knowledge Base at <a href="http://go.microsoft.com/fwlink/p/?linkid=167966">http://go.microsoft.com/fwlink/p/?linkid=167966</a>.




## -see-also




<a href="https://msdn.microsoft.com/08c354a6-5cc0-405c-91cf-dca55b87b49a">IVdsVolumeShrink</a>
 

 

