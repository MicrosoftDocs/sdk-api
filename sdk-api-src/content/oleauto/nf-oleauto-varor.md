---
UID: NF:oleauto.VarOr
title: VarOr function (oleauto.h)
description: Performs a logical disjunction on two variants.
helpviewer_keywords: ["VarOr","VarOr function [Automation]","_oa96_VarOr","automat.varor","oleauto/VarOr"]
old-location: automat\varor.htm
tech.root: automat
ms.assetid: 8c161755-4fdd-48bd-9dc4-6510cc9ce8ab
ms.date: 12/05/2018
ms.keywords: VarOr, VarOr function [Automation], _oa96_VarOr, automat.varor, oleauto/VarOr
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
 - VarOr
 - oleauto/VarOr
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
 - VarOr
---

# VarOr function


## -description

Performs a logical disjunction on two variants.

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
<th><i>pvarLeft</i></th>
<th><i>pvarRight</i></th>
<th><i>pvarResult</i></th>
</tr>
<tr>
<td>TRUE</td>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>TRUE</td>
<td>FALSE</td>
<td>TRUE</td>
</tr>
<tr>
<td>TRUE</td>
<td>NULL</td>
<td>TRUE</td>
</tr>
<tr>
<td>FALSE</td>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>FALSE</td>
<td>FALSE</td>
<td>FALSE</td>
</tr>
<tr>
<td>FALSE</td>
<td>NULL</td>
<td>NULL</td>
</tr>
<tr>
<td>NULL</td>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>NULL</td>
<td>FALSE</td>
<td>NULL</td>
</tr>
<tr>
<td>NULL</td>
<td>NULL</td>
<td>NULL</td>
</tr>
</table>

