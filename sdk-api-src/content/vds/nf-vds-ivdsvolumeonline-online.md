---
UID: NF:vds.IVdsVolumeOnline.Online
title: IVdsVolumeOnline::Online
author: windows-sdk-content
description: Returns a volume to the healthy state, if possible. This method is supported only for dynamic disks.
old-location: base\ivdsvolumeonline_online.htm
tech.root: VDS
ms.assetid: 8a207e61-5a13-41ad-bad9-11ddf2844a9b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsVolumeOnline interface,Online method, IVdsVolumeOnline.Online, IVdsVolumeOnline::Online, Online, Online method, Online method,IVdsVolumeOnline interface, base.ivdsvolumeonline_online, vds/IVdsVolumeOnline::Online
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
 - IVdsVolumeOnline.Online
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
- IVdsVolumeOnline.Online
: 
---

# IVdsVolumeOnline::Online


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns a volume to the healthy state, if possible. This method is supported only for dynamic disks.


## -parameters






## -returns



This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
<dt><b>VDS_S_NO_NOTIFICATION</b></dt>
<dt>0x00042517L</dt>
</dl>
</td>
<td width="60%">
No volume arrival notification was received. You may need to call <a href="https://msdn.microsoft.com/ca6a1143-b5f0-49e5-8505-836c565aabcf">IVdsService::Refresh</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This method is not supported for basic disks.

</td>
</tr>
</table>
 




## -remarks



Despite its name, this method does not bring a volume online. It attempts to return a volume on a dynamic disk to a healthy state. 

This method checks whether the volume has a missing disk, plex, or RAID-5 column and attempts to make any needed repairs. 

To bring the volume online, call <a href="https://msdn.microsoft.com/1de3bbd7-cd81-42f9-9e25-48a0a07e9ccc">IVdsVolumeMF::Mount</a>.

To take the volume offline, call <a href="https://msdn.microsoft.com/1ef5a1e6-0e41-4077-9ae8-fe266f2623cc">IVdsVolumeMF::Dismount</a> with the <i>bPermanent</i> parameter set to <b>TRUE</b>. 




## -see-also




<a href="https://msdn.microsoft.com/f2b7d9aa-e42c-4d6b-92e0-9d9bfbde1a42">IVdsVolumeOnline</a>
 

 

