---
UID: NF:imapi2fs.IFileSystemImage.get_VolumeNameUDF
title: IFileSystemImage::get_VolumeNameUDF (imapi2fs.h)
description: Retrieves the volume name for the UDF system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_VolumeNameUDF method","IFileSystemImage.get_VolumeNameUDF","IFileSystemImage::get_VolumeNameUDF","get_VolumeNameUDF","get_VolumeNameUDF method [IMAPI]","get_VolumeNameUDF method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_volumenameudf","imapi2fs/IFileSystemImage::get_VolumeNameUDF"]
old-location: imapi\ifilesystemimage_get_volumenameudf.htm
tech.root: imapi
ms.assetid: d034f8cb-38f5-42ab-8952-e4a76dc1f27d
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_VolumeNameUDF method, IFileSystemImage.get_VolumeNameUDF, IFileSystemImage::get_VolumeNameUDF, get_VolumeNameUDF, get_VolumeNameUDF method [IMAPI], get_VolumeNameUDF method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_volumenameudf, imapi2fs/IFileSystemImage::get_VolumeNameUDF
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
 - IFileSystemImage::get_VolumeNameUDF
 - imapi2fs/IFileSystemImage::get_VolumeNameUDF
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
 - IFileSystemImage.get_VolumeNameUDF
---

# IFileSystemImage::get_VolumeNameUDF


## -description

Retrieves the volume name for the UDF system image.

## -parameters

### -param pVal [out]

String that contains the volume name for the UDF system image.

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

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumename">IFileSystemImage::get_VolumeName</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumenameiso9660">IFileSystemImage::get_VolumeNameISO9660</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumenamejoliet">IFileSystemImage::get_VolumeNameJoliet</a>