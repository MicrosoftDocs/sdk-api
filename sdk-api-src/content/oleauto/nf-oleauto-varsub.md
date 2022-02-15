---
UID: NF:oleauto.VarSub
title: VarSub function (oleauto.h)
description: Subtracts two variants.
helpviewer_keywords: ["VarSub","VarSub function [Automation]","_oa96_VarSub","automat.varsub","oleauto/VarSub"]
old-location: automat\varsub.htm
tech.root: automat
ms.assetid: 395cc5fe-8694-47a9-8e92-1768c300ba7e
ms.date: 12/05/2018
ms.keywords: VarSub, VarSub function [Automation], _oa96_VarSub, automat.varsub, oleauto/VarSub
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
 - VarSub
 - oleauto/VarSub
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
 - VarSub
---

# VarSub function


## -description

Subtracts two variants.

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
<td>Subtraction</td>
</tr>
<tr>
<td>One expression is a string and the other a character</td>
<td>Subtraction</td>
</tr>
<tr>
<td>One expression is numeric and the other a string</td>
<td>Subtraction</td>
</tr>
<tr>
<td>Both expressions are numeric</td>
<td>Subtraction</td>
</tr>
<tr>
<td>Either expression is null</td>
<td>Null</td>
</tr>
<tr>
<td>Both expressions are empty</td>
<td>Empty string</td>
</tr>
</table>

