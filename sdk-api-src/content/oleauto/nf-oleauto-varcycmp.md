---
UID: NF:oleauto.VarCyCmp
title: VarCyCmp function (oleauto.h)
description: Compares two variants of type currency.
helpviewer_keywords: ["VarCyCmp","VarCyCmp function [Automation]","_oa96_VarCyCmp","automat.varcycmp","oleauto/VarCyCmp"]
old-location: automat\varcycmp.htm
tech.root: automat
ms.assetid: 18146c52-c4ca-48b6-b0be-d93a849cee96
ms.date: 12/05/2018
ms.keywords: VarCyCmp, VarCyCmp function [Automation], _oa96_VarCyCmp, automat.varcycmp, oleauto/VarCyCmp
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
 - VarCyCmp
 - oleauto/VarCyCmp
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
 - VarCyCmp
---

# VarCyCmp function


## -description

Compares two variants of type currency.

## -parameters

### -param cyLeft [in]

The first variant.

### -param cyRight [in]

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
<i>cyLeft</i> is less than <i>cyRight</i>.


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
<i>cyLeft</i> is greater than <i>cyRight</i>.


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

