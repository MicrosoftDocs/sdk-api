---
UID: NF:imapi2fs.IFileSystemImage.get_StrictFileSystemCompliance
title: IFileSystemImage::get_StrictFileSystemCompliance (imapi2fs.h)
description: Determines the compliance level for creating and developing the file-system image. (Get)
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_StrictFileSystemCompliance method","IFileSystemImage.get_StrictFileSystemCompliance","IFileSystemImage::get_StrictFileSystemCompliance","get_StrictFileSystemCompliance","get_StrictFileSystemCompliance method [IMAPI]","get_StrictFileSystemCompliance method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_strictfilesystemcompliance","imapi2fs/IFileSystemImage::get_StrictFileSystemCompliance"]
old-location: imapi\ifilesystemimage_get_strictfilesystemcompliance.htm
tech.root: imapi
ms.assetid: 07139ef3-ffd5-4035-afa9-6212808a6fbc
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_StrictFileSystemCompliance method, IFileSystemImage.get_StrictFileSystemCompliance, IFileSystemImage::get_StrictFileSystemCompliance, get_StrictFileSystemCompliance, get_StrictFileSystemCompliance method [IMAPI], get_StrictFileSystemCompliance method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_strictfilesystemcompliance, imapi2fs/IFileSystemImage::get_StrictFileSystemCompliance
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
 - IFileSystemImage::get_StrictFileSystemCompliance
 - imapi2fs/IFileSystemImage::get_StrictFileSystemCompliance
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
 - IFileSystemImage.get_StrictFileSystemCompliance
---

# IFileSystemImage::get_StrictFileSystemCompliance


## -description

Determines the compliance level for creating and developing the file-system image.

## -parameters

### -param pVal [out]

Is VARIANT_TRUE if the file system images are created in strict compliance with applicable standards.  

Is VARIANT_FALSE if the compliance standards are relaxed to be compatible with IMAPI version 1.0.

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



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_strictfilesystemcompliance">IFileSystemImage::put_StrictFileSystemCompliance</a>
