---
UID: NF:oleauto.VarCat
title: VarCat function (oleauto.h)
description: Concatenates two variants and returns the result.
helpviewer_keywords: ["VarCat","VarCat function [Automation]","_oa96_VarCat","automat.varcat","oleauto/VarCat"]
old-location: automat\varcat.htm
tech.root: automat
ms.assetid: 2e94516e-de36-407a-a1fe-6a6e66641c17
ms.date: 12/05/2018
ms.keywords: VarCat, VarCat function [Automation], _oa96_VarCat, automat.varcat, oleauto/VarCat
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VarCat
 - oleauto/VarCat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarCat
---

# VarCat function


## -description

Concatenates two variants and returns the result.

## -parameters

### -param pvarLeft [in]

The first variant.

### -param pvarRight [in]

The second variant.

### -param pvarResult [out]

The result variant.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The function operates as follows.

<table>
<tr>
<th>Condition</th>
<th>Result</th>
</tr>
<tr>
<td>Both expressions are strings</td>
<td>Concatenated</td>
</tr>
<tr>
<td>Both expressions are null</td>
<td>Null</td>
</tr>
<tr>
<td>One expression is null and the other is not null</td>
<td>The non-null type</td>
</tr>
<tr>
<td>Either expression is a Boolean</td>
<td> FALSE equal to 1 or TRUE equal to -1</td>
</tr>
<tr>
<td>Either expression is VT_ERROR</td>
<td>Null</td>
</tr>
<tr>
<td>Both expressions are numeric</td>
<td>Concatenated and  returned as a string</td>
</tr>
<tr>
<td>One expression is numeric and the other a string</td>
<td>Concatenated</td>
</tr>
<tr>
<td>Either expression is a date</td>
<td>Date</td>
</tr>
<tr>
<td>Both expressions are empty</td>
<td>Empty string</td>
</tr>
</table>

