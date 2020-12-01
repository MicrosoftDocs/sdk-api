---
UID: NF:imapi2fs.IProgressItems.get_Item
title: IProgressItems::get_Item (imapi2fs.h)
description: Retrieves the specified progress item from the collection.
helpviewer_keywords: ["IProgressItems interface [IMAPI]","get_Item method","IProgressItems.get_Item","IProgressItems::get_Item","get_Item","get_Item method [IMAPI]","get_Item method [IMAPI]","IProgressItems interface","imapi.iprogressitems_get_item","imapi2fs/IProgressItems::get_Item"]
old-location: imapi\iprogressitems_get_item.htm
tech.root: imapi
ms.assetid: 74d8e74d-0af6-457a-a16b-f959757b5a86
ms.date: 12/05/2018
ms.keywords: IProgressItems interface [IMAPI],get_Item method, IProgressItems.get_Item, IProgressItems::get_Item, get_Item, get_Item method [IMAPI], get_Item method [IMAPI],IProgressItems interface, imapi.iprogressitems_get_item, imapi2fs/IProgressItems::get_Item
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
 - IProgressItems::get_Item
 - imapi2fs/IProgressItems::get_Item
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
 - IProgressItems.get_Item
---

# IProgressItems::get_Item


## -description

Retrieves the specified progress item from the collection.

## -parameters

### -param Index [in]

Zero-based index number corresponding to a progress item in the collection.

### -param item [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a> interface associated with the specified index value.

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
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
</table>

## -remarks

To enumerate all progress items, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitems-get__newenum">IProgressItems::get__NewEnum</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitems-progressitemfromblock">IProgressItems::ProgressItemFromBlock</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitems-progressitemfromdescription">IProgressItems::ProgressItemFromDescription</a>