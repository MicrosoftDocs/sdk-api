---
UID: NF:imapi2fs.IFileSystemImage.ChooseImageDefaults
title: IFileSystemImage::ChooseImageDefaults
author: windows-sdk-content
description: Sets the default file system types and the image size based on the current media.
old-location: imapi\ifilesystemimage_chooseimagedefaults.htm
tech.root: imapi
ms.assetid: 9211b8af-9331-4d0d-a6f5-f52f8db42e8c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ChooseImageDefaults, ChooseImageDefaults method [IMAPI], ChooseImageDefaults method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],ChooseImageDefaults method, IFileSystemImage.ChooseImageDefaults, IFileSystemImage::ChooseImageDefaults, imapi.ifilesystemimage_chooseimagedefaults, imapi2fs/IFileSystemImage::ChooseImageDefaults
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFileSystemImage.ChooseImageDefaults
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImage::ChooseImageDefaults


## -description


Sets the default file system types and the image size based on the current media.


## -parameters




### -param discRecorder [in]

An <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> the identifies the device that contains the current media.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
The media is not compatible or of unknown physical format.

Value: 0xC0AA0203

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
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</b></dt>
</dl>
</td>
<td width="60%">
The specified disc does not contain one of the supported file systems.

Value: 0xC0AAB151

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>
 

 

