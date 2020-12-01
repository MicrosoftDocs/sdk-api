---
UID: NF:imapi2fs.IFileSystemImage2.put_BootImageOptionsArray
title: IFileSystemImage2::put_BootImageOptionsArray (imapi2fs.h)
description: Sets the boot option array that will be utilized to generate the file system image. Unlike IFileSystemImage::put_BootImageOptions, this method will not create a complete copy of each boot options array element, but instead use references to each element.
helpviewer_keywords: ["IFileSystemImage2 interface [IMAPI]","put_BootImageOptionsArray method","IFileSystemImage2.put_BootImageOptionsArray","IFileSystemImage2::put_BootImageOptionsArray","imapi.ifilesystemimage2_put_bootimageoptionsarray","imapi2fs/IFileSystemImage2::put_BootImageOptionsArray","put_BootImageOptionsArray","put_BootImageOptionsArray method [IMAPI]","put_BootImageOptionsArray method [IMAPI]","IFileSystemImage2 interface"]
old-location: imapi\ifilesystemimage2_put_bootimageoptionsarray.htm
tech.root: imapi
ms.assetid: 0b827f6a-8e40-4d9d-bec6-8d7f33dade43
ms.date: 12/05/2018
ms.keywords: IFileSystemImage2 interface [IMAPI],put_BootImageOptionsArray method, IFileSystemImage2.put_BootImageOptionsArray, IFileSystemImage2::put_BootImageOptionsArray, imapi.ifilesystemimage2_put_bootimageoptionsarray, imapi2fs/IFileSystemImage2::put_BootImageOptionsArray, put_BootImageOptionsArray, put_BootImageOptionsArray method [IMAPI], put_BootImageOptionsArray method [IMAPI],IFileSystemImage2 interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFileSystemImage2::put_BootImageOptionsArray
 - imapi2fs/IFileSystemImage2::put_BootImageOptionsArray
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
 - IFileSystemImage2.put_BootImageOptionsArray
---

# IFileSystemImage2::put_BootImageOptionsArray


## -description

Sets the boot option array that will be utilized to generate the file system image. Unlike <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions">IFileSystemImage::put_BootImageOptions</a>, this method will not create  a complete copy of each  boot options array element, but instead use references to each element.

## -parameters

### -param newVal [in]

List of <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions">IBootOptions</a> interfaces of the boot images that will be utilized to generate the file system image. Each element of the list is a <b>VARIANT</b> of the type <b>VT_DISPATCH</b>.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
No such interface supported.

Value: 0x80004002

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

## -remarks

The <b>SAFEARRAY</b> must be a one dimensional array. A zero-size array is allowed, but it will result in a regular, non-bootable disc.

The boot images sequence on the disc will match the sequence specified in the <b>SAFEARRAY</b>. Both <b>put_BootImageOptionsArray</b> and <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions">put_BootImageOptions</a> are used for specifying the boot image, the latter function being invoked before the disc image created takes effect.

The <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage2-get_bootimageoptionsarray">get_BootImageOptionsArray</a> and <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_bootimageoptions">get_BootImageOptions</a> functions will retrieve the result of the last calls of put_BootImageOptionsArray or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions">put_BootImageOptions</a>. The use of these functions should be synchronized.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2">IFileSystemImage2</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage2-get_bootimageoptionsarray">IFileSystemImage2::get_BootImageOptionsArray</a>