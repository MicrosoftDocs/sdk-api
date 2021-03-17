---
UID: NF:imapi2fs.IFileSystemImage.get_VolumeName
title: IFileSystemImage::get_VolumeName (imapi2fs.h)
description: Retrieves the volume name for this file system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_VolumeName method","IFileSystemImage.get_VolumeName","IFileSystemImage::get_VolumeName","get_VolumeName","get_VolumeName method [IMAPI]","get_VolumeName method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_volumename","imapi2fs/IFileSystemImage::get_VolumeName"]
old-location: imapi\ifilesystemimage_get_volumename.htm
tech.root: imapi
ms.assetid: 95d5738b-a720-4f47-b3a0-97f7474b051a
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_VolumeName method, IFileSystemImage.get_VolumeName, IFileSystemImage::get_VolumeName, get_VolumeName, get_VolumeName method [IMAPI], get_VolumeName method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_volumename, imapi2fs/IFileSystemImage::get_VolumeName
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
 - IFileSystemImage::get_VolumeName
 - imapi2fs/IFileSystemImage::get_VolumeName
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
 - IFileSystemImage.get_VolumeName
---

# IFileSystemImage::get_VolumeName


## -description

Retrieves the volume name for this file system image.

## -parameters

### -param pVal [out]

String that contains the volume name for this file system image.

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

To set the volume name, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_volumename">IFileSystemImage::put_VolumeName</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_importedvolumename">IFileSystemImage::get_ImportedVolumeName</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_volumename">IFileSystemImage::put_VolumeName</a>