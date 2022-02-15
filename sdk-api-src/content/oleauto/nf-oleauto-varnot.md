---
UID: NF:oleauto.VarNot
title: VarNot function (oleauto.h)
description: Performs the bitwise not negation operation on a variant.
helpviewer_keywords: ["VarNot","VarNot function [Automation]","_oa96_VarNot","automat.varnot","oleauto/VarNot"]
old-location: automat\varnot.htm
tech.root: automat
ms.assetid: e3825905-2a28-4283-bb65-0273572f3150
ms.date: 12/05/2018
ms.keywords: VarNot, VarNot function [Automation], _oa96_VarNot, automat.varnot, oleauto/VarNot
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
 - VarNot
 - oleauto/VarNot
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
 - VarNot
---

# VarNot function


## -description

Performs the bitwise not negation operation on a variant.

## -parameters

### -param pvarIn [in]

The variant.

### -param pvarResult [out]

The result variant.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The function operates as follows.

<table>
<tr>
<th><i>pvarIn</i></th>
<th><i>pvarResult</i></th>
</tr>
<tr>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>FALSE</td>
<td>TRUE</td>
</tr>
<tr>
<td>NULL</td>
<td>NULL</td>
</tr>
</table>

