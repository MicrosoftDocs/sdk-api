---
UID: NF:oleauto.VarDiv
title: VarDiv function (oleauto.h)
description: Returns the result from dividing two variants.
helpviewer_keywords: ["VarDiv","VarDiv function [Automation]","_oa96_VarDiv","automat.vardiv","oleauto/VarDiv"]
old-location: automat\vardiv.htm
tech.root: automat
ms.assetid: 63cd466d-da23-4c61-ba7c-899f56f02245
ms.date: 12/05/2018
ms.keywords: VarDiv, VarDiv function [Automation], _oa96_VarDiv, automat.vardiv, oleauto/VarDiv
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
 - VarDiv
 - oleauto/VarDiv
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
 - VarDiv
---

# VarDiv function


## -description

Returns the result from dividing two variants.

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
<td>Both expressions are strings, dates, characters, or boolean values</td>
<td>Double</td>
</tr>
<tr>
<td>One expression is a string and the other a character</td>
<td>Division and a double is returned</td>
</tr>
<tr>
<td>One expression is numeric and the other a string</td>
<td>Division and a double is returned</td>
</tr>
<tr>
<td>Both expressions are numeric</td>
<td>Division and a double is returned</td>
</tr>
<tr>
<td>Either expression is null</td>
<td>Null</td>
</tr>
<tr>
<td><i>pvarRight</i> is empty and <i>pvarLeft</i> is not empty</td>
<td>DISP_E_DIVBYZERO</td>
</tr>
<tr>
<td><i>pvarLeft</i> is empty and <i>pvarRight</i> is not empty</td>
<td>0 as type double</td>
</tr>
<tr>
<td>Both expressions are empty</td>
<td>DISP_E_OVERFLOW</td>
</tr>
</table>

