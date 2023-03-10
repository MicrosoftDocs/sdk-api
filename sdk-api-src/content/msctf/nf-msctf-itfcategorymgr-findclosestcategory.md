---
UID: NF:msctf.ITfCategoryMgr.FindClosestCategory
title: ITfCategoryMgr::FindClosestCategory (msctf.h)
description: ITfCategoryMgr::FindClosestCategory method
helpviewer_keywords: ["FindClosestCategory","FindClosestCategory method [Text Services Framework]","FindClosestCategory method [Text Services Framework]","ITfCategoryMgr interface","ITfCategoryMgr interface [Text Services Framework]","FindClosestCategory method","ITfCategoryMgr.FindClosestCategory","ITfCategoryMgr::FindClosestCategory","_tsf_itfcategorymgr_findclosestcategory_ref","msctf/ITfCategoryMgr::FindClosestCategory","tsf.itfcategorymgr_findclosestcategory"]
old-location: tsf\itfcategorymgr_findclosestcategory.htm
tech.root: TSF
ms.assetid: 16a78457-b89c-43ef-8604-fd6c2f93f928
ms.date: 12/05/2018
ms.keywords: FindClosestCategory, FindClosestCategory method [Text Services Framework], FindClosestCategory method [Text Services Framework],ITfCategoryMgr interface, ITfCategoryMgr interface [Text Services Framework],FindClosestCategory method, ITfCategoryMgr.FindClosestCategory, ITfCategoryMgr::FindClosestCategory, _tsf_itfcategorymgr_findclosestcategory_ref, msctf/ITfCategoryMgr::FindClosestCategory, tsf.itfcategorymgr_findclosestcategory
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
 - ITfCategoryMgr::FindClosestCategory
 - msctf/ITfCategoryMgr::FindClosestCategory
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
 - ITfCategoryMgr.FindClosestCategory
---

# ITfCategoryMgr::FindClosestCategory


## -description

Finds the category closest to the specified GUID from a list of categories.

## -parameters

### -param rguid [in]

Specifies the address of the GUID for which to find the closest category.

### -param pcatid [out]

Pointer to the **GUID** that receives the CATID for the closest category.

### -param ppcatidList [in]

Pointer to a pointer that specifies an array of CATIDs to search for the closest category.

### -param ulCount [in]

Specifies the number of elements in the array of the <i>ppcatidList</i> parameter.

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
The method obtained the closest category from the list of categories, or the method was unable to obtain a category from the list and indicates this with a <i>pcatid</i> parameter pointer to GUID_NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to find a category for the specified GUID and signals this with a <i>pcatid</i> parameter pointer to GUID_NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method cannot access the internal table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>pcatid</i> parameter was <b>NULL</b> on input, or the list of categories contained a <b>NULL</b> element when the <i>ulCount</i> parameter was nonzero.

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

## -remarks

The closest category to a **GUID** is chosen in one of two modes. In the first mode, the method receives a non-empty category list. It chooses the first matching **CATID** from that list or GUID_NULL if the list does not contain a category that contains the **GUID** . In the second mode, it receives an empty category list. It chooses the first category that contains the **GUID** or GUID_NULL if no category contains the **GUID** .

## -see-also

[ITfCategoryMgr interface](nn-msctf-itfcategorymgr.md), [ITfCategoryMgr::EnumCategoriesInItem](nf-msctf-itfcategorymgr-enumcategoriesinitem.md), [ITfCategoryMgr::EnumItemsInCategory](nf-msctf-itfcategorymgr-enumitemsincategory.md), [ITfCategoryMgr::RegisterCategory](nf-msctf-itfcategorymgr-registercategory.md)

