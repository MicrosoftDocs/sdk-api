---
UID: NF:imapi2fs.IFileSystemImageResult2.get_ModifiedBlocks
title: IFileSystemImageResult2::get_ModifiedBlocks (imapi2fs.h)
description: Retrieves the list of modified blocks in the result image.
helpviewer_keywords: ["IFileSystemImageResult2 interface [IMAPI]","get_ModifiedBlocks method","IFileSystemImageResult2.get_ModifiedBlocks","IFileSystemImageResult2::get_ModifiedBlocks","get_ModifiedBlocks","get_ModifiedBlocks method [IMAPI]","get_ModifiedBlocks method [IMAPI]","IFileSystemImageResult2 interface","imapi.ifilesystemimageresult2_get_modifiedblocks","imapi2fs/IFileSystemImageResult2::get_ModifiedBlocks"]
old-location: imapi\ifilesystemimageresult2_get_modifiedblocks.htm
tech.root: imapi
ms.assetid: 2148ba3f-f334-43cb-965a-37b078419e0c
ms.date: 12/05/2018
ms.keywords: IFileSystemImageResult2 interface [IMAPI],get_ModifiedBlocks method, IFileSystemImageResult2.get_ModifiedBlocks, IFileSystemImageResult2::get_ModifiedBlocks, get_ModifiedBlocks, get_ModifiedBlocks method [IMAPI], get_ModifiedBlocks method [IMAPI],IFileSystemImageResult2 interface, imapi.ifilesystemimageresult2_get_modifiedblocks, imapi2fs/IFileSystemImageResult2::get_ModifiedBlocks
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IFileSystemImageResult2::get_ModifiedBlocks
 - imapi2fs/IFileSystemImageResult2::get_ModifiedBlocks
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
 - IFileSystemImageResult2.get_ModifiedBlocks
---

# IFileSystemImageResult2::get_ModifiedBlocks


## -description

Retrieves the list of modified blocks in the result image.

## -parameters

### -param pVal [out]

Pointer to an <a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist">IBlockRangeList</a> interface representing the modified block ranges in the result image.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>

## -remarks

This method returns <b>E_NOTIMPL</b> if the entire result image must be recorded. If this method returns a successful return code, it is sufficient to record only the sectors described by <a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist">IBlockRangeList</a> returned in <i>pVal</i>. It is highly recommended to record the sector ranges in exactly the same order as they are listed in <b>IBlockRangeList</b>.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult2">IFileSystemImageResult2</a>