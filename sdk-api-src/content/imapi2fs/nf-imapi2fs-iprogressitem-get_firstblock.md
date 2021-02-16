---
UID: NF:imapi2fs.IProgressItem.get_FirstBlock
title: IProgressItem::get_FirstBlock (imapi2fs.h)
description: Retrieves the first block number in this segment of the result image.
helpviewer_keywords: ["IProgressItem interface [IMAPI]","get_FirstBlock method","IProgressItem.get_FirstBlock","IProgressItem::get_FirstBlock","get_FirstBlock","get_FirstBlock method [IMAPI]","get_FirstBlock method [IMAPI]","IProgressItem interface","imapi.iprogressitem_get_firstblock","imapi2fs/IProgressItem::get_FirstBlock"]
old-location: imapi\iprogressitem_get_firstblock.htm
tech.root: imapi
ms.assetid: 9c1c5932-0301-4752-871d-609d3c128906
ms.date: 12/05/2018
ms.keywords: IProgressItem interface [IMAPI],get_FirstBlock method, IProgressItem.get_FirstBlock, IProgressItem::get_FirstBlock, get_FirstBlock, get_FirstBlock method [IMAPI], get_FirstBlock method [IMAPI],IProgressItem interface, imapi.iprogressitem_get_firstblock, imapi2fs/IProgressItem::get_FirstBlock
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
 - IProgressItem::get_FirstBlock
 - imapi2fs/IProgressItem::get_FirstBlock
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
 - IProgressItem.get_FirstBlock
---

# IProgressItem::get_FirstBlock


## -description

Retrieves the first block number in this segment of the result image.

## -parameters

### -param block [out]

First block number of this segment.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitem-get_blockcount">IProgressItem::get_BlockCount</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitem-get_lastblock">IProgressItem::get_LastBlock</a>