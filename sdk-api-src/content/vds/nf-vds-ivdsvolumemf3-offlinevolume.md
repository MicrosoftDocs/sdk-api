---
UID: NF:vds.IVdsVolumeMF3.OfflineVolume
title: IVdsVolumeMF3::OfflineVolume
author: windows-sdk-content
description: Takes the volume offline by using the IOCTL_VOLUME_OFFLINE control code.
old-location: base\ivdsvolumemf3_offlinevolume.htm
old-project: VDS
ms.assetid: d7f699c6-6f1c-445d-80b4-3576102d5b5f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVdsVolumeMF3 interface,OfflineVolume method, IVdsVolumeMF3.OfflineVolume, IVdsVolumeMF3::OfflineVolume, OfflineVolume, OfflineVolume method, OfflineVolume method,IVdsVolumeMF3 interface, base.ivdsvolumemf3_offlinevolume, vds/IVdsVolumeMF3::OfflineVolume
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsVolumeMF3.OfflineVolume
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolumeMF3::OfflineVolume


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Takes the volume offline by using the <a href="https://msdn.microsoft.com/library/windows/hardware/ff561431">IOCTL_VOLUME_OFFLINE</a> control code.


## -parameters






## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
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
</table>
 




## -remarks



If the volume is already offline, the <b>OfflineVolume</b> method returns S_OK.

When a volume is offline, all read, write, and IOCTL requests fail with 
    <b>ERROR_NOT_READY</b>. You cannot take the system or boot volume offline.

When a volume is online, all requests sent to the volume are honored.

When a volume that is online 
    is dismounted, the next call to open the volume causes it to be mounted. Taking the volume offline prevents the 
    dismounted volume from being mounted again. To dismount a volume, use the <a href="https://msdn.microsoft.com/1ef5a1e6-0e41-4077-9ae8-fe266f2623cc">IVdsVolumeMF::Dismount</a> method.




## -see-also




<a href="https://msdn.microsoft.com/46b8ff26-c00b-45ef-ac30-0aa82786bf9b">IVdsVolumeMF3</a>
 

 

