---
UID: NF:imapi2fs.IFileSystemImage.ChooseImageDefaultsForMediaType
title: IFileSystemImage::ChooseImageDefaultsForMediaType
author: windows-sdk-content
description: Sets the default file system types and the image size based on the specified media type.
old-location: imapi\ifilesystemimage_chooseimagedefaultsformediatype.htm
old-project: imapi
ms.assetid: 1d327da0-d0b3-4fcf-9773-ff5ea1eeea1c
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ChooseImageDefaultsForMediaType, ChooseImageDefaultsForMediaType method [IMAPI], ChooseImageDefaultsForMediaType method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],ChooseImageDefaultsForMediaType method, IFileSystemImage.ChooseImageDefaultsForMediaType, IFileSystemImage::ChooseImageDefaultsForMediaType, imapi.ifilesystemimage_chooseimagedefaultsformediatype, imapi2fs/IFileSystemImage::ChooseImageDefaultsForMediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFileSystemImage.ChooseImageDefaultsForMediaType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::ChooseImageDefaultsForMediaType


## -description


Sets the default file system types and the image size based on the specified media type. 


## -parameters




### -param value [in]

Identifies the physical media type that will receive the burn image. For possible values, see the <a href="https://msdn.microsoft.com/027c5e09-6cf7-4d7c-8381-07dc92cc43c5">IMAPI_MEDIA_PHYSICAL_TYPE</a> enumeration type.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGE_TOO_BIG</b></dt>
</dl>
</td>
<td width="60%">
Value specified for FreeMediaBlocks property is too small for estimated image size based on current data. 

Value: 0xC0AAB121

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>
 

 

