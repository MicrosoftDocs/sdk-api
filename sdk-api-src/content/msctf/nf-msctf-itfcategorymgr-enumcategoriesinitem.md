---
UID: NF:msctf.ITfCategoryMgr.EnumCategoriesInItem
title: ITfCategoryMgr::EnumCategoriesInItem (msctf.h)
description: ITfCategoryMgr::EnumCategoriesInItem method
helpviewer_keywords: ["EnumCategoriesInItem","EnumCategoriesInItem method [Text Services Framework]","EnumCategoriesInItem method [Text Services Framework]","ITfCategoryMgr interface","ITfCategoryMgr interface [Text Services Framework]","EnumCategoriesInItem method","ITfCategoryMgr.EnumCategoriesInItem","ITfCategoryMgr::EnumCategoriesInItem","_tsf_itfcategorymgr_enumcategoriesinitem_ref","msctf/ITfCategoryMgr::EnumCategoriesInItem","tsf.itfcategorymgr_enumcategoriesinitem"]
old-location: tsf\itfcategorymgr_enumcategoriesinitem.htm
tech.root: TSF
ms.assetid: 271e5fbe-54e2-47e3-97d4-cd4211b92080
ms.date: 12/05/2018
ms.keywords: EnumCategoriesInItem, EnumCategoriesInItem method [Text Services Framework], EnumCategoriesInItem method [Text Services Framework],ITfCategoryMgr interface, ITfCategoryMgr interface [Text Services Framework],EnumCategoriesInItem method, ITfCategoryMgr.EnumCategoriesInItem, ITfCategoryMgr::EnumCategoriesInItem, _tsf_itfcategorymgr_enumcategoriesinitem_ref, msctf/ITfCategoryMgr::EnumCategoriesInItem, tsf.itfcategorymgr_enumcategoriesinitem
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCategoryMgr::EnumCategoriesInItem
 - msctf/ITfCategoryMgr::EnumCategoriesInItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfCategoryMgr.EnumCategoriesInItem
---

# ITfCategoryMgr::EnumCategoriesInItem


## -description

Obtains an IEnumGUID interface that enumerates all categories to which the specified GUID belongs.

## -parameters

### -param rguid [in]

Contains a GUID value that identifies the item to enumerate the categories for.

### -param ppEnum [out]

Pointer to an IEnumGUID interface pointer that receives the enumerator.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppEnum</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to perform the operation.

</td>
</tr>
</table>

## -see-also

[ITfCategoryMgr interface](nn-msctf-itfcategorymgr.md), [ITfCategoryMgr::EnumItemsInCategory](nf-msctf-itfcategorymgr-enumitemsincategory.md), [ITfCategoryMgr::RegisterCategory](nf-msctf-itfcategorymgr-registercategory.md)

