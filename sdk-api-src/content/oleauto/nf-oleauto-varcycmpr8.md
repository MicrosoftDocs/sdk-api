---
UID: NF:oleauto.VarCyCmpR8
title: VarCyCmpR8 function (oleauto.h)
description: Compares a variant of type currency with a value of type double.
helpviewer_keywords: ["VarCyCmpR8","VarCyCmpR8 function [Automation]","_oa96_VarCyCmpR8","automat.varcycmpr8","oleauto/VarCyCmpR8"]
old-location: automat\varcycmpr8.htm
tech.root: automat
ms.assetid: 391ace93-7f08-4fa3-a897-1f4012fe631b
ms.date: 12/05/2018
ms.keywords: VarCyCmpR8, VarCyCmpR8 function [Automation], _oa96_VarCyCmpR8, automat.varcycmpr8, oleauto/VarCyCmpR8
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
 - VarCyCmpR8
 - oleauto/VarCyCmpR8
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
 - VarCyCmpR8
---

# VarCyCmpR8 function


## -description

Compares a variant of type currency with a value of type double.

## -parameters

### -param cyLeft [in]

The first variant.

### -param dblRight [in]

The second variant.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_LT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
<i>cyLeft</i> is less than <i>dblRight</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_EQ</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The two parameters are equal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_GT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
<i>cyLeft</i> is greater than <i>dblRight</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_NULL</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Either expression is null.

</td>
</tr>
</table>

