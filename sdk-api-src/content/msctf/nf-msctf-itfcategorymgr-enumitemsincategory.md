---
UID: NF:msctf.ITfCategoryMgr.EnumItemsInCategory
title: ITfCategoryMgr::EnumItemsInCategory (msctf.h)
description: ITfCategoryMgr::EnumItemsInCategory method
helpviewer_keywords: ["EnumItemsInCategory","EnumItemsInCategory method [Text Services Framework]","EnumItemsInCategory method [Text Services Framework]","ITfCategoryMgr interface","ITfCategoryMgr interface [Text Services Framework]","EnumItemsInCategory method","ITfCategoryMgr.EnumItemsInCategory","ITfCategoryMgr::EnumItemsInCategory","_tsf_itfcategorymgr_enumitemsincategory_ref","msctf/ITfCategoryMgr::EnumItemsInCategory","tsf.itfcategorymgr_enumitemsincategory"]
old-location: tsf\itfcategorymgr_enumitemsincategory.htm
tech.root: TSF
ms.assetid: 88b123d8-86aa-40ae-8777-1b33cfbb953a
ms.date: 12/05/2018
ms.keywords: EnumItemsInCategory, EnumItemsInCategory method [Text Services Framework], EnumItemsInCategory method [Text Services Framework],ITfCategoryMgr interface, ITfCategoryMgr interface [Text Services Framework],EnumItemsInCategory method, ITfCategoryMgr.EnumItemsInCategory, ITfCategoryMgr::EnumItemsInCategory, _tsf_itfcategorymgr_enumitemsincategory_ref, msctf/ITfCategoryMgr::EnumItemsInCategory, tsf.itfcategorymgr_enumitemsincategory
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
 - ITfCategoryMgr::EnumItemsInCategory
 - msctf/ITfCategoryMgr::EnumItemsInCategory
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
 - ITfCategoryMgr.EnumItemsInCategory
---

# ITfCategoryMgr::EnumItemsInCategory


## -description

Obtains an IEnumGUID interface that enumerates all GUIDs included in the specified category.

## -parameters

### -param rcatid [in]

Contains a GUID value that identifies the category to enumerate the items for.

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

[ITfCategoryMgr interface](nn-msctf-itfcategorymgr.md), [ITfCategoryMgr::EnumCategoriesInItem](nf-msctf-itfcategorymgr-enumcategoriesinitem.md), [ITfCategoryMgr::RegisterCategory](nf-msctf-itfcategorymgr-registercategory.md)

