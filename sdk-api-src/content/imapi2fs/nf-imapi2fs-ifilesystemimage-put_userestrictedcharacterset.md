---
UID: NF:imapi2fs.IFileSystemImage.put_UseRestrictedCharacterSet
title: IFileSystemImage::put_UseRestrictedCharacterSet (imapi2fs.h)
description: Determines if file and directory names should be restricted to using only CP_ANSI characters.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","put_UseRestrictedCharacterSet method","IFileSystemImage.put_UseRestrictedCharacterSet","IFileSystemImage::put_UseRestrictedCharacterSet","imapi.ifilesystemimage_put_userestrictedcharacterset","imapi2fs/IFileSystemImage::put_UseRestrictedCharacterSet","put_UseRestrictedCharacterSet","put_UseRestrictedCharacterSet method [IMAPI]","put_UseRestrictedCharacterSet method [IMAPI]","IFileSystemImage interface"]
old-location: imapi\ifilesystemimage_put_userestrictedcharacterset.htm
tech.root: imapi
ms.assetid: de64ef3d-94b3-4d97-946e-8331c5a39f4b
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_UseRestrictedCharacterSet method, IFileSystemImage.put_UseRestrictedCharacterSet, IFileSystemImage::put_UseRestrictedCharacterSet, imapi.ifilesystemimage_put_userestrictedcharacterset, imapi2fs/IFileSystemImage::put_UseRestrictedCharacterSet, put_UseRestrictedCharacterSet, put_UseRestrictedCharacterSet method [IMAPI], put_UseRestrictedCharacterSet method [IMAPI],IFileSystemImage interface
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
 - IFileSystemImage::put_UseRestrictedCharacterSet
 - imapi2fs/IFileSystemImage::put_UseRestrictedCharacterSet
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
 - IFileSystemImage.put_UseRestrictedCharacterSet
---

# IFileSystemImage::put_UseRestrictedCharacterSet


## -description

Determines if file and directory names should be restricted to using only CP_ANSI characters. <div class="alert"><b>Note</b>  <b>IFileSystemImage::put_UseRestrictedCharacterSet</b> has been deprecated. Implementing this method is not recommended.</div>
<div> </div>

## -parameters

### -param newVal [in]

Set to VARIANT_TRUE to restrict file and directory names to use only CP_ANSI characters. Otherwise, VARIANT_FALSE. The default is VARIANT_FALSE.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

Setting this property does not affect files or directories already in the file system image.

You can change the value of this property only when the result stream is not active.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem">IFileSystemImage::CreateDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem">IFileSystemImage::CreateFileItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_userestrictedcharacterset">IFileSystemImage::get_UseRestrictedCharacterSet</a>