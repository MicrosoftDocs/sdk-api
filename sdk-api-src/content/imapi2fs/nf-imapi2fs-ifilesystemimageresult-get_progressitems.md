---
UID: NF:imapi2fs.IFileSystemImageResult.get_ProgressItems
title: IFileSystemImageResult::get_ProgressItems (imapi2fs.h)
description: Retrieves the progress item block mapping collection.
helpviewer_keywords: ["IFileSystemImageResult interface [IMAPI]","get_ProgressItems method","IFileSystemImageResult.get_ProgressItems","IFileSystemImageResult::get_ProgressItems","get_ProgressItems","get_ProgressItems method [IMAPI]","get_ProgressItems method [IMAPI]","IFileSystemImageResult interface","imapi.ifilesystemimageresult_get_progressitems","imapi2fs/IFileSystemImageResult::get_ProgressItems"]
old-location: imapi\ifilesystemimageresult_get_progressitems.htm
tech.root: imapi
ms.assetid: c4ef572d-7e18-4537-847c-419441befe00
ms.date: 12/05/2018
ms.keywords: IFileSystemImageResult interface [IMAPI],get_ProgressItems method, IFileSystemImageResult.get_ProgressItems, IFileSystemImageResult::get_ProgressItems, get_ProgressItems, get_ProgressItems method [IMAPI], get_ProgressItems method [IMAPI],IFileSystemImageResult interface, imapi.ifilesystemimageresult_get_progressitems, imapi2fs/IFileSystemImageResult::get_ProgressItems
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
 - IFileSystemImageResult::get_ProgressItems
 - imapi2fs/IFileSystemImageResult::get_ProgressItems
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
 - IFileSystemImageResult.get_ProgressItems
---

# IFileSystemImageResult::get_ProgressItems


## -description

Retrieves the progress item block mapping collection.

## -parameters

### -param pVal [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a> interface that contains a collection of progress items. Each progress item identifies the blocks written since the previous progress status was taken.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate necessary memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems">IEnumProgressItems</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a>