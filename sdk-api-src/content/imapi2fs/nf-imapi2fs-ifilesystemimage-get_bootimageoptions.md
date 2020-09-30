---
UID: NF:imapi2fs.IFileSystemImage.get_BootImageOptions
title: IFileSystemImage::get_BootImageOptions (imapi2fs.h)
description: Retrieves the boot image that you want to add to the file system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_BootImageOptions method","IFileSystemImage.get_BootImageOptions","IFileSystemImage::get_BootImageOptions","get_BootImageOptions","get_BootImageOptions method [IMAPI]","get_BootImageOptions method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_bootimageoptions","imapi2fs/IFileSystemImage::get_BootImageOptions"]
old-location: imapi\ifilesystemimage_get_bootimageoptions.htm
tech.root: imapi
ms.assetid: b9721313-a2b0-4d91-af10-7932bd2d01be
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_BootImageOptions method, IFileSystemImage.get_BootImageOptions, IFileSystemImage::get_BootImageOptions, get_BootImageOptions, get_BootImageOptions method [IMAPI], get_BootImageOptions method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_bootimageoptions, imapi2fs/IFileSystemImage::get_BootImageOptions
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
 - IFileSystemImage::get_BootImageOptions
 - imapi2fs/IFileSystemImage::get_BootImageOptions
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
 - IFileSystemImage.get_BootImageOptions
---

# IFileSystemImage::get_BootImageOptions


## -description

Retrieves the boot image that you want to add to the file system image.

## -parameters

### -param pVal [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions">IBootOptions</a> interface of the boot image to add to the disc. Is <b>NULL</b> if a boot image has not been specified.

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
<dt><b>IMAPI_E_BOOT_OBJECT_CONFLICT</b></dt>
</dl>
</td>
<td width="60%">
A boot object can only be included in an initial disc image.

Value: 0xC0AAB149

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_BOOT_IMAGE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The boot object could not be added to the image.

Value: 0xC0AAB148

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions">IBootOptions</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions">IFileSystemImage::put_BootImageOptions</a>