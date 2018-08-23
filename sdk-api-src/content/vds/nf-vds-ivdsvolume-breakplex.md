---
UID: NF:vds.IVdsVolume.BreakPlex
title: IVdsVolume::BreakPlex
author: windows-sdk-content
description: Removes a specified plex from the current volume.
old-location: base\ivdsvolume_breakplex.htm
old-project: vds
ms.assetid: c7e42aa4-3233-40e9-b537-043eecd192ad
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BreakPlex, BreakPlex method [VDS], BreakPlex method [VDS],IVdsVolume interface, IVdsVolume interface [VDS],BreakPlex method, IVdsVolume.BreakPlex, IVdsVolume::BreakPlex, base.ivdsvolume_breakplex, vds/IVdsVolume::BreakPlex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVolume.BreakPlex
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolume::BreakPlex


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Removes a specified 
   plex from the current volume. The interface pointer for the new 
   <a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">volume object</a> can be retrieved by calling 
   <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> through the 
   <i>ppAsync</i> parameter. The 
   <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure returned contains the volume 
   object interface pointer in the <b>bvp.pVolumeUnk</b> member.


## -parameters




### -param plexId [in]

The GUID of the plex to be broken.


### -param ppAsync [out]

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer, 
      which VDS initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or 
      query the status of the operation.

If you call <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> on this method and a success HRESULT value is returned, 
      you must release the interfaces returned in the 
      <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="_com_succeeded">SUCCEEDED</a> and <a href="_com_failed">FAILED</a> macros defined in Winerror.h.


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
The plex was broken successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_NOT_ONLINE</b></dt>
<dt>0x8004243DL</dt>
</dl>
</td>
<td width="60%">
The volume is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_NOT_A_MIRROR</b></dt>
<dt>0x80042445L</dt>
</dl>
</td>
<td width="60%">
The volume is not a mirror.

</td>
</tr>
</table>
 




## -remarks



This operation is not valid for basic volumes, which have exactly one plex.

Use this method to break a mirror. The broken plex becomes a new volume. If the remaining plex is stale or 
    missing, VDS stops the operation and returns an error. Note that VDS dismounts the volume during the 
    operation.

A boot or system plex—essentially, the plex used to boot the computer—is not valid for 
    <b>plexId</b>. When passed such a plex, VDS stops the operation and returns an error.

Implementers must return a pointer to the <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> 
     interface for this method, regardless of whether the call initiates an asynchronous operation.




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a>



<a href="https://msdn.microsoft.com/a02ee0a6-ac29-406c-9fc0-4f632d32424f">IVdsVolume</a>



<a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a>
 

 

