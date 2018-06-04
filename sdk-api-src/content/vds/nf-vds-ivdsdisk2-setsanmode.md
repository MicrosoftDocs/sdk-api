---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IVdsDisk2::SetSANMode


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Sets the SAN mode of a disk to offline or online.<div class="alert"><b>Note</b>  Starting with Windows Vista with Service Pack 1 (SP1), this method is superseded by the <a href="https://msdn.microsoft.com/b3366bc7-18ca-4a90-b4e7-e6213a7cc002">IVdsDiskOnline::Online</a> and <a href="https://msdn.microsoft.com/3f27dd46-2fa1-4522-9d35-db78255c6d11">IVdsDiskOnline::Offline</a> methods.</div>
<div> </div>



## -parameters




### -param bEnable [in]

Specify <b>TRUE</b> for online or <b>FALSE</b> for offline.


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
The SAN mode was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_FAILED_TO_OFFLINE_DISK</b></dt>
<dt>0x80042597L</dt>
</dl>
</td>
<td width="60%">
The offline operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_FAILED_TO_ONLINE_DISK</b></dt>
<dt>0x80042596L</dt>
</dl>
</td>
<td width="60%">
The online operation failed.

</td>
</tr>
</table>
 




## -remarks



Setting the SAN mode of a disk to offline is called "offlining" the disk. Setting it to online is called "onlining" the disk.

<b>Windows Vista:  </b>Setting the SAN mode of a disk to offline also makes the disk read-only. Setting it to online also makes the disk read-write.




## -see-also




<a href="https://msdn.microsoft.com/9fb8a08e-412d-415a-aa27-cc0180599903">IVdsDisk2</a>
 

 

