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

# IFileSystemImage2 interface


## -description


 Use this interface to write multiple boot entries or boot images  required for the EFI/UEFI support. For example, boot media with boot straps for both Windows XP and Windows Vista.<div class="alert"><b>Note</b>  The <b>IFileSystemImage2</b> interface is currently only available with  Windows Vista with Service Pack 1 (SP1) and  Windows Server 2008.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemImage2</b> interface inherits from <a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>. <b>IFileSystemImage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSystemImage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31e4c8e8-7a00-41e7-b3cf-78dbc10fc3d2">get_BootImageOptionsArray</a>
</td>
<td align="left" width="63%">
Retrieves the boot option array that will be utilized to generate the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b827f6a-8e40-4d9d-bec6-8d7f33dade43">put_BootImageOptionsArray</a>
</td>
<td align="left" width="63%">
Sets the boot option array that will be utilized to generate the file system image.

</td>
</tr>
</table> 


## -remarks



 Boot entries are limited by the interface to 32 per disc.	The boot image must be supplied to IMAPIv2FS by outside applications who invoke IMAPIv2FS to build the bootable disc.

Section Entry Extension is not supported by IMAPIv2FS at this time.





## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>
 

 

