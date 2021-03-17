---
UID: NF:imapi2fs.IFileSystemImage.CreateResultImage
title: IFileSystemImage::CreateResultImage (imapi2fs.h)
description: Create the result object that contains the file system and file data.
helpviewer_keywords: ["CreateResultImage","CreateResultImage method [IMAPI]","CreateResultImage method [IMAPI]","IFileSystemImage interface","IFileSystemImage interface [IMAPI]","CreateResultImage method","IFileSystemImage.CreateResultImage","IFileSystemImage::CreateResultImage","imapi.ifilesystemimage_createresultimage","imapi2fs/IFileSystemImage::CreateResultImage"]
old-location: imapi\ifilesystemimage_createresultimage.htm
tech.root: imapi
ms.assetid: 6f7d2438-5c80-4461-8b48-646f0ca44498
ms.date: 12/05/2018
ms.keywords: CreateResultImage, CreateResultImage method [IMAPI], CreateResultImage method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],CreateResultImage method, IFileSystemImage.CreateResultImage, IFileSystemImage::CreateResultImage, imapi.ifilesystemimage_createresultimage, imapi2fs/IFileSystemImage::CreateResultImage
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
 - IFileSystemImage::CreateResultImage
 - imapi2fs/IFileSystemImage::CreateResultImage
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
 - IFileSystemImage.CreateResultImage
---

# IFileSystemImage::CreateResultImage


## -description

Create the result object that contains the file system and file data.

## -parameters

### -param resultStream [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a> interface of the image result.

Client applications can stream the image to media or other long-term storage devices, such as disk drives.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -remarks

 Currently, <b>IFileSystemImage::CreateResultImage</b> will require disc media access as a result of  a previous <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc">IFileSystemImage::IdentifyFileSystemsOnDisc</a> method call. To resolve this issue, it is recommended that another  <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> object be created specifically for the <b>IFileSystemImage::IdentifyFileSystemsOnDisc</b> operation.

The resulting stream can be saved as an ISO file if the file system is generated in a single session and has a start address of zero.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_filesystemstocreate">IFileSystemImage::get_FileSystemsToCreate</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_filesystemstocreate">IFileSystemImage::put_FileSystemsToCreate</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-chooseimagedefaults">IFilesystemImage::ChooseImageDefaults</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-chooseimagedefaultsformediatype">IFilesystemImage::ChooseImageDefaultsForMediaType</a>