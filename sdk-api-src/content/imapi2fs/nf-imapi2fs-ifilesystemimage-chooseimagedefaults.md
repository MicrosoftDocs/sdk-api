---
UID: NF:imapi2fs.IFileSystemImage.ChooseImageDefaults
title: IFileSystemImage::ChooseImageDefaults (imapi2fs.h)
description: Sets the default file system types and the image size based on the current media.
helpviewer_keywords: ["ChooseImageDefaults","ChooseImageDefaults method [IMAPI]","ChooseImageDefaults method [IMAPI]","IFileSystemImage interface","IFileSystemImage interface [IMAPI]","ChooseImageDefaults method","IFileSystemImage.ChooseImageDefaults","IFileSystemImage::ChooseImageDefaults","imapi.ifilesystemimage_chooseimagedefaults","imapi2fs/IFileSystemImage::ChooseImageDefaults"]
old-location: imapi\ifilesystemimage_chooseimagedefaults.htm
tech.root: imapi
ms.assetid: 9211b8af-9331-4d0d-a6f5-f52f8db42e8c
ms.date: 12/05/2018
ms.keywords: ChooseImageDefaults, ChooseImageDefaults method [IMAPI], ChooseImageDefaults method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],ChooseImageDefaults method, IFileSystemImage.ChooseImageDefaults, IFileSystemImage::ChooseImageDefaults, imapi.ifilesystemimage_chooseimagedefaults, imapi2fs/IFileSystemImage::ChooseImageDefaults
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSystemImage::ChooseImageDefaults
 - imapi2fs/IFileSystemImage::ChooseImageDefaults
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.ChooseImageDefaults
---

# IFileSystemImage::ChooseImageDefaults


## -description

Sets the default file system types and the image size based on the current media.

## -parameters

### -param discRecorder [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> the identifies the device that contains the current media.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>