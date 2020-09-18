---
UID: NF:imapi2fs.IFileSystemImage.get_UseRestrictedCharacterSet
title: IFileSystemImage::get_UseRestrictedCharacterSet (imapi2fs.h)
description: Determines if the file and directory names use a restricted character.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_UseRestrictedCharacterSet method","IFileSystemImage.get_UseRestrictedCharacterSet","IFileSystemImage::get_UseRestrictedCharacterSet","get_UseRestrictedCharacterSet","get_UseRestrictedCharacterSet method [IMAPI]","get_UseRestrictedCharacterSet method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_userestrictedcharacterset","imapi2fs/IFileSystemImage::get_UseRestrictedCharacterSet"]
old-location: imapi\ifilesystemimage_get_userestrictedcharacterset.htm
tech.root: imapi
ms.assetid: 106615e8-f1d4-4ac9-b96a-bcda204f5e2c
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_UseRestrictedCharacterSet method, IFileSystemImage.get_UseRestrictedCharacterSet, IFileSystemImage::get_UseRestrictedCharacterSet, get_UseRestrictedCharacterSet, get_UseRestrictedCharacterSet method [IMAPI], get_UseRestrictedCharacterSet method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_userestrictedcharacterset, imapi2fs/IFileSystemImage::get_UseRestrictedCharacterSet
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
 - IFileSystemImage::get_UseRestrictedCharacterSet
 - imapi2fs/IFileSystemImage::get_UseRestrictedCharacterSet
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
 - IFileSystemImage.get_UseRestrictedCharacterSet
---

# IFileSystemImage::get_UseRestrictedCharacterSet


## -description

Determines if the file and directory names use a restricted character.

## -parameters

### -param pVal [out]

Is VARIANT_TRUE if the file and directory names to add to the file system image must consist of characters that map directly to CP_ANSI (code points 32 through 127). Otherwise, VARIANT_FALSE.

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



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem">IFileSystemImage::CreateDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem">IFileSystemImage::CreateFileItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_userestrictedcharacterset">IFileSystemImage::put_UseRestrictedCharacterSet</a>