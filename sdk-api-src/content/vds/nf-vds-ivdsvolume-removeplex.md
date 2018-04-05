---
UID: NF:vds.IVdsVolume.RemovePlex
title: IVdsVolume::RemovePlex method
author: windows-driver-content
description: Removes one or more specified plexes from the current volume, releasing the extents.
old-location: base\ivdsvolume_removeplex.htm
old-project: VDS
ms.assetid: 724f80e7-4656-4956-aaad-9f778329f139
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IVdsVolume, IVdsVolume interface [VDS], RemovePlex method, IVdsVolume::RemovePlex, RemovePlex method [VDS], RemovePlex method [VDS], IVdsVolume interface, RemovePlex,IVdsVolume.RemovePlex, base.ivdsvolume_removeplex, vds/IVdsVolume::RemovePlex
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsVolume.RemovePlex
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolume::RemovePlex method


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]


   Removes one or more 
   specified plexes from the current volume, releasing the extents.


## -parameters




### -param plexId [in]

The GUID of the plex to be removed.


### -param ppAsync [out]


      The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer, which VDS 
      initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or query the 
      status of the operation.


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
The plex was removed successfully.

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
The volume is not accessible.

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




    This operation cannot remove the last plex of a volume. Instead, use the 
    <a href="https://msdn.microsoft.com/6cc7cb6d-4495-41b7-8fe5-d2e1f574ed70">IVdsVolume::Delete</a> method to remove the last 
    remaining volume (the sole plex). This method is not valid for basic volumes, which have exactly one plex.


    VDS does not dismount the volume when it removes a plex.
    


     Implementers must return a pointer to the <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface for 
     this method, regardless of whether the call initiates an asynchronous operation.




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/a02ee0a6-ac29-406c-9fc0-4f632d32424f">IVdsVolume</a>



<a href="https://msdn.microsoft.com/6cc7cb6d-4495-41b7-8fe5-d2e1f574ed70">IVdsVolume::Delete</a>
 

 

