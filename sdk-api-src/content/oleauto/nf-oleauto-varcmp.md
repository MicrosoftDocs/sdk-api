---
UID: NF:oleauto.VarCmp
title: VarCmp function (oleauto.h)
description: Compares two variants.
helpviewer_keywords: ["NORM_IGNORECASE","NORM_IGNOREKANATYPE","NORM_IGNOREKASHIDA","NORM_IGNORENONSPACE","NORM_IGNORESYMBOLS","NORM_IGNOREWIDTH","VarCmp","VarCmp function [Automation]","_oa96_VarCmp","automat.varcmp","oleauto/VarCmp"]
old-location: automat\varcmp.htm
tech.root: automat
ms.assetid: 00b96fa7-446c-450b-bd06-a966e1acb5ce
ms.date: 12/05/2018
ms.keywords: NORM_IGNORECASE, NORM_IGNOREKANATYPE, NORM_IGNOREKASHIDA, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREWIDTH, VarCmp, VarCmp function [Automation], _oa96_VarCmp, automat.varcmp, oleauto/VarCmp
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
 - VarCmp
 - oleauto/VarCmp
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
 - VarCmp
---

# VarCmp function


## -description

Compares two variants.

## -parameters

### -param pvarLeft [in]

The first variant.

### -param pvarRight [in]

The second variant.

### -param lcid [in]

The locale identifier.

### -param dwFlags [in]

The compare results option.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORECASE"></a><a id="norm_ignorecase"></a><dl>
<dt><b>NORM_IGNORECASE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Ignore case.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORENONSPACE"></a><a id="norm_ignorenonspace"></a><dl>
<dt><b>NORM_IGNORENONSPACE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Ignore nonspace characters.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORESYMBOLS"></a><a id="norm_ignoresymbols"></a><dl>
<dt><b>NORM_IGNORESYMBOLS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Ignore symbols.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREWIDTH"></a><a id="norm_ignorewidth"></a><dl>
<dt><b>NORM_IGNOREWIDTH</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Ignore string width.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREKANATYPE"></a><a id="norm_ignorekanatype"></a><dl>
<dt><b>NORM_IGNOREKANATYPE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Ignore Kana type.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREKASHIDA"></a><a id="norm_ignorekashida"></a><dl>
<dt><b>NORM_IGNOREKASHIDA</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Ignore Arabic kashida characters.

</td>
</tr>
</table>

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
<i>pvarLeft</i> is less than <i>pvarRight</i>.

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
The parameters are equal.

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
<i>pvarLeft</i> is greater than <i>pvarRight</i>.

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
Either expression is NULL.

</td>
</tr>
</table>

## -remarks

The function only compares the value of the variant types. It compares strings, integers, and floating points, but not arrays or records.

NORM_IGNOREWIDTH causes <b>VarCmp</b> to ignore the difference between half-width and full-width characters, as the following example demonstrates: 

"Ｃａｔ"== "cat"

The full-width form is a formatting distinction used in Chinese and Japanese scripts.

## -see-also

<a href="/previous-versions/windows/desktop/automat/automation-programming-reference">Automation Programming Reference</a>



<a href="/previous-versions/windows/desktop/automat/conversion-and-manipulation-functions">Conversion and Manipulation Functions</a>



<a href="/previous-versions/windows/desktop/automat/variant-arithmetic-functions">Variant Arithmetic Functions</a>