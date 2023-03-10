---
UID: NF:imapi2fs.IFileSystemImage.get_VolumeNameISO9660
title: IFileSystemImage::get_VolumeNameISO9660 (imapi2fs.h)
description: Retrieves the volume name for the ISO9660 system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_VolumeNameISO9660 method","IFileSystemImage.get_VolumeNameISO9660","IFileSystemImage::get_VolumeNameISO9660","get_VolumeNameISO9660","get_VolumeNameISO9660 method [IMAPI]","get_VolumeNameISO9660 method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_volumenameiso9660","imapi2fs/IFileSystemImage::get_VolumeNameISO9660"]
old-location: imapi\ifilesystemimage_get_volumenameiso9660.htm
tech.root: imapi
ms.assetid: 9f41c273-d56a-4e8f-aa9f-e2a49741f7e3
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_VolumeNameISO9660 method, IFileSystemImage.get_VolumeNameISO9660, IFileSystemImage::get_VolumeNameISO9660, get_VolumeNameISO9660, get_VolumeNameISO9660 method [IMAPI], get_VolumeNameISO9660 method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_volumenameiso9660, imapi2fs/IFileSystemImage::get_VolumeNameISO9660
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
 - IFileSystemImage::get_VolumeNameISO9660
 - imapi2fs/IFileSystemImage::get_VolumeNameISO9660
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
 - IFileSystemImage.get_VolumeNameISO9660
---

# IFileSystemImage::get_VolumeNameISO9660


## -description

Retrieves the volume name for the ISO9660 system image.

## -parameters

### -param pVal [out]

String that contains the volume name for the ISO9660 system image.

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



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumenamejoliet">IFileSystemImage::get_VolumeNameJoliet</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumenameudf">IFileSystemImage::get_VolumeNameUDF</a>