---
UID: NF:imapi2fs.IFileSystemImage.get_ImportedVolumeName
title: IFileSystemImage::get_ImportedVolumeName (imapi2fs.h)
description: Retrieves the volume name provided from an imported file system.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_ImportedVolumeName method","IFileSystemImage.get_ImportedVolumeName","IFileSystemImage::get_ImportedVolumeName","get_ImportedVolumeName","get_ImportedVolumeName method [IMAPI]","get_ImportedVolumeName method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_importedvolumename","imapi2fs/IFileSystemImage::get_ImportedVolumeName"]
old-location: imapi\ifilesystemimage_get_importedvolumename.htm
tech.root: imapi
ms.assetid: 57d66dd3-2525-4102-bba7-00bad76a3d9c
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_ImportedVolumeName method, IFileSystemImage.get_ImportedVolumeName, IFileSystemImage::get_ImportedVolumeName, get_ImportedVolumeName, get_ImportedVolumeName method [IMAPI], get_ImportedVolumeName method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_importedvolumename, imapi2fs/IFileSystemImage::get_ImportedVolumeName
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
 - IFileSystemImage::get_ImportedVolumeName
 - imapi2fs/IFileSystemImage::get_ImportedVolumeName
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
 - IFileSystemImage.get_ImportedVolumeName
---

# IFileSystemImage::get_ImportedVolumeName


## -description

Retrieves the volume name provided from an imported file system.

## -parameters

### -param pVal [out]

String that contains the volume name provided from an imported file system. Is <b>NULL</b> until a file system is imported.

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
</table>

## -remarks

The imported volume name is provided for user information and is not automatically carried forward to subsequent sessions.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumename">IFileSystemImage::get_VolumeName</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_volumename">IFileSystemImage::put_VolumeName</a>