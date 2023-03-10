---
UID: NF:oleauto.VarIdiv
title: VarIdiv function (oleauto.h)
description: Converts two variants of any type to integers then returns the result from dividing them.
helpviewer_keywords: ["VarIdiv","VarIdiv function [Automation]","_oa96_VarIdiv","automat.varidiv","oleauto/VarIdiv"]
old-location: automat\varidiv.htm
tech.root: automat
ms.assetid: dd76b96f-b616-420f-9f26-d88004574411
ms.date: 12/05/2018
ms.keywords: VarIdiv, VarIdiv function [Automation], _oa96_VarIdiv, automat.varidiv, oleauto/VarIdiv
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
 - VarIdiv
 - oleauto/VarIdiv
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
 - VarIdiv
---

# VarIdiv function


## -description

Converts two variants of any type to integers then returns the result from dividing them.

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
<td>Division and an integer is returned</td>
</tr>
<tr>
<td>One expression is a string and the other a character</td>
<td>Division</td>
</tr>
<tr>
<td>One expression is numeric and the other a string</td>
<td>Division</td>
</tr>
<tr>
<td>Both expressions are numeric</td>
<td>Division</td>
</tr>
<tr>
<td>Either expression is null</td>
<td>Null</td>
</tr>
<tr>
<td>Both expressions are empty</td>
<td>DISP_E_DIVBYZERO</td>
</tr>
</table>

