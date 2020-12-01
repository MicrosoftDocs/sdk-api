---
UID: NF:tapi3if.ITCollection2.Add
title: ITCollection2::Add (tapi3if.h)
description: The Add method inserts a new item into the collection at the specified index.
helpviewer_keywords: ["Add","Add method [TAPI 2.2]","Add method [TAPI 2.2]","ITCollection2 interface","ITCollection2 interface [TAPI 2.2]","Add method","ITCollection2.Add","ITCollection2::Add","_tapi3_itcollection2_add","tapi3.itcollection2_add","tapi3if/ITCollection2::Add"]
old-location: tapi3\itcollection2_add.htm
tech.root: tapi3
ms.assetid: 96c26f76-3835-4140-8379-91171fc4ad37
ms.date: 12/05/2018
ms.keywords: Add, Add method [TAPI 2.2], Add method [TAPI 2.2],ITCollection2 interface, ITCollection2 interface [TAPI 2.2],Add method, ITCollection2.Add, ITCollection2::Add, _tapi3_itcollection2_add, tapi3.itcollection2_add, tapi3if/ITCollection2::Add
req.header: tapi3if.h
req.include-header: 
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
 - ITCollection2::Add
 - tapi3if/ITCollection2::Add
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
 - ITCollection2.Add
---

# ITCollection2::Add


## -description

The 
<b>Add</b> method inserts a new item into the collection at the specified index.

## -parameters

### -param Index [in]

Specifies the location in the collection where the item should be added.

### -param pVariant [in]

Pointer to a <b>VARIANT</b> containing the item to add.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Index</i> parameter does not specify a valid index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to reallocate the collection.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection2">ITCollection2</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcollection2-remove">Remove</a>