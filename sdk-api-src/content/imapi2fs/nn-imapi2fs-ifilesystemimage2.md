---
UID: NN:imapi2fs.IFileSystemImage2
title: IFileSystemImage2
author: windows-sdk-content
description: Use this interface to write multiple boot entries or boot images required for the EFI/UEFI support. For example, boot media with boot straps for both Windows XP and Windows Vista.
old-location: imapi\ifilesystemimage2.htm
tech.root: imapi
ms.assetid: c38995b7-6f32-4489-bb6c-0e3561b11f81
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IFileSystemImage2, IFileSystemImage2 interface [IMAPI], IFileSystemImage2 interface [IMAPI],described, imapi.ifilesystemimage2, imapi2fs/IFileSystemImage2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

