---
UID: NF:shobjidl_core.ICategorizer.CompareCategory
title: ICategorizer::CompareCategory (shobjidl_core.h)
description: Determines the relative order of two items in their item identifier lists, and hence in the UI.
helpviewer_keywords: ["CompareCategory","CompareCategory method [Windows Shell]","CompareCategory method [Windows Shell]","ICategorizer interface","ICategorizer interface [Windows Shell]","CompareCategory method","ICategorizer.CompareCategory","ICategorizer::CompareCategory","inet_ICategorizer_CompareCategory","shell.ICategorizer_CompareCategory","shobjidl_core/ICategorizer::CompareCategory"]
old-location: shell\ICategorizer_CompareCategory.htm
tech.root: shell
ms.assetid: 25775fa5-595d-4911-9cd4-47fde429b923
ms.date: 12/05/2018
ms.keywords: CompareCategory, CompareCategory method [Windows Shell], CompareCategory method [Windows Shell],ICategorizer interface, ICategorizer interface [Windows Shell],CompareCategory method, ICategorizer.CompareCategory, ICategorizer::CompareCategory, inet_ICategorizer_CompareCategory, shell.ICategorizer_CompareCategory, shobjidl_core/ICategorizer::CompareCategory
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICategorizer::CompareCategory
 - shobjidl_core/ICategorizer::CompareCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICategorizer.CompareCategory
---

# ICategorizer::CompareCategory


## -description

Determines the relative order of two items in their item identifier lists, and hence in the UI.

## -parameters

### -param csfFlags

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-catsort_flags">CATSORT_FLAGS</a></b>

A flag that specifies how the comparison should be performed. The parameter should be one of the values in <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-catsort_flags">CATSORT_FLAGS</a>.

### -param dwCategoryId1

Type: <b>DWORD</b>

A <b>DWORD</b> that specifies the first category identifier to use in the comparison.

### -param dwCategoryId2

Type: <b>DWORD</b>

A <b>DWORD</b> that specifies the second category identifier to use in the comparison.

## -returns

Type: <b>HRESULT</b>

If this method is successful, the CODE field of the HRESULT contains a value that specifies the outcome of the comparison, otherwise it returns a COM error code.

## -remarks

The following table shows the values returned in the CODE field of the HRESULT.

    			


<table class="clsStd">
<tr>
<td>Less than zero </td>
<td>The first item should precede the second (<i>dwCategoryId1</i> &lt; <i>dwCategoryId2</i>).</td>
</tr>
<tr>
<td>Greater than zero </td>
<td>The first item should follow the second (<i>dwCategoryId1</i> &gt; <i>dwCategoryId2</i>).</td>
</tr>
<tr>
<td>Zero </td>
<td>The two items are the same (<i>dwCategoryId1</i> = <i>dwCategoryId2</i>).</td>
</tr>
</table>