---
UID: NF:imapi2fs.IFileSystemImageResult.get_BlockSize
title: IFileSystemImageResult::get_BlockSize (imapi2fs.h)
description: Retrieves the size, in bytes, of a block of data.
helpviewer_keywords: ["IFileSystemImageResult interface [IMAPI]","get_BlockSize method","IFileSystemImageResult.get_BlockSize","IFileSystemImageResult::get_BlockSize","get_BlockSize","get_BlockSize method [IMAPI]","get_BlockSize method [IMAPI]","IFileSystemImageResult interface","imapi.ifilesystemimageresult_get_blocksize","imapi2fs/IFileSystemImageResult::get_BlockSize"]
old-location: imapi\ifilesystemimageresult_get_blocksize.htm
tech.root: imapi
ms.assetid: fe6d14d7-f3ae-4634-b8b4-1793f8007826
ms.date: 12/05/2018
ms.keywords: IFileSystemImageResult interface [IMAPI],get_BlockSize method, IFileSystemImageResult.get_BlockSize, IFileSystemImageResult::get_BlockSize, get_BlockSize, get_BlockSize method [IMAPI], get_BlockSize method [IMAPI],IFileSystemImageResult interface, imapi.ifilesystemimageresult_get_blocksize, imapi2fs/IFileSystemImageResult::get_BlockSize
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
 - IFileSystemImageResult::get_BlockSize
 - imapi2fs/IFileSystemImageResult::get_BlockSize
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
 - IFileSystemImageResult.get_BlockSize
---

# IFileSystemImageResult::get_BlockSize


## -description

Retrieves the size, in bytes, of a block of data.

## -parameters

### -param pVal [out]

Number of bytes in a block.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_totalblocks">IFileSystemImageResult::get_TotalBlocks</a>