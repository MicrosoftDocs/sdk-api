---
UID: NF:imapi2fs.IFileSystemImage.get_VolumeNameJoliet
title: IFileSystemImage::get_VolumeNameJoliet (imapi2fs.h)
description: Retrieves the volume name for the Joliet system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_VolumeNameJoliet method","IFileSystemImage.get_VolumeNameJoliet","IFileSystemImage::get_VolumeNameJoliet","get_VolumeNameJoliet","get_VolumeNameJoliet method [IMAPI]","get_VolumeNameJoliet method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_volumenamejoliet","imapi2fs/IFileSystemImage::get_VolumeNameJoliet"]
old-location: imapi\ifilesystemimage_get_volumenamejoliet.htm
tech.root: imapi
ms.assetid: 5300763d-9f2f-4562-bb5e-61fcf485b086
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_VolumeNameJoliet method, IFileSystemImage.get_VolumeNameJoliet, IFileSystemImage::get_VolumeNameJoliet, get_VolumeNameJoliet, get_VolumeNameJoliet method [IMAPI], get_VolumeNameJoliet method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_volumenamejoliet, imapi2fs/IFileSystemImage::get_VolumeNameJoliet
f1_keywords:
- imapi2fs/IFileSystemImage.get_VolumeNameJoliet
dev_langs:
- c++
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
- IFileSystemImage.get_VolumeNameJoliet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileSystemImage::get_VolumeNameJoliet


## -description


Retrieves the volume name for the Joliet system image.


## -parameters




### -param pVal [out]

String that contains the volume name for the Joliet system image.


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




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumename">IFileSystemImage::get_VolumeName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumenameiso9660">IFileSystemImage::get_VolumeNameISO9660</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumenameudf">IFileSystemImage::get_VolumeNameUDF</a>
 

 

