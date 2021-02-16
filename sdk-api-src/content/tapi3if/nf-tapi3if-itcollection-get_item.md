---
UID: NF:tapi3if.ITCollection.get_Item
title: ITCollection::get_Item (tapi3if.h)
description: The get_Item method, given an index, returns an item in the collection.
helpviewer_keywords: ["ITCollection interface [TAPI 2.2]","get_Item method","ITCollection.get_Item","ITCollection::get_Item","_tapi3_itcollection_get_item","get_Item","get_Item method [TAPI 2.2]","get_Item method [TAPI 2.2]","ITCollection interface","tapi3.itcollection_get_item","tapi3if/ITCollection::get_Item"]
old-location: tapi3\itcollection_get_item.htm
tech.root: tapi3
ms.assetid: f4e6de7e-99c4-415f-b3b4-7e8bf1f082fc
ms.date: 12/05/2018
ms.keywords: ITCollection interface [TAPI 2.2],get_Item method, ITCollection.get_Item, ITCollection::get_Item, _tapi3_itcollection_get_item, get_Item, get_Item method [TAPI 2.2], get_Item method [TAPI 2.2],ITCollection interface, tapi3.itcollection_get_item, tapi3if/ITCollection::get_Item
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITCollection::get_Item
 - tapi3if/ITCollection::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCollection.get_Item
---

# ITCollection::get_Item


## -description

The 
<b>get_Item</b> method, given an index, returns an item in the collection.

## -parameters

### -param Index [in]

Index of item to be retrieved.

### -param pVariant [out]

Pointer to item returned.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>