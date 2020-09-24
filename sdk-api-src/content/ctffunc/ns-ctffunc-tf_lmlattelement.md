---
UID: NS:ctffunc.TF_LMLATTELEMENT
title: TF_LMLATTELEMENT (ctffunc.h)
description: The TF_LMLATTELEMENT structure contains information about a lattice element. A lattice element is used in speech recognition. This structure is used with the IEnumTfLatticeElements::Next method.
helpviewer_keywords: ["TF_LMLATTELEMENT","TF_LMLATTELEMENT structure [Text Services Framework]","_tsf_tf_lmlattelement_ref","ctffunc/TF_LMLATTELEMENT","tsf.tf_lmlattelement"]
old-location: tsf\tf_lmlattelement.htm
tech.root: TSF
ms.assetid: 55cc631f-c9ab-4ca8-ab5b-43e8a2e88fc9
ms.date: 12/05/2018
ms.keywords: TF_LMLATTELEMENT, TF_LMLATTELEMENT structure [Text Services Framework], _tsf_tf_lmlattelement_ref, ctffunc/TF_LMLATTELEMENT, tsf.tf_lmlattelement
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TF_LMLATTELEMENT
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_LMLATTELEMENT
 - ctffunc/TF_LMLATTELEMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ctffunc.h
api_name:
 - TF_LMLATTELEMENT
---

# TF_LMLATTELEMENT structure


## -description

The <b>TF_LMLATTELEMENT</b> structure contains information about a lattice element. A lattice element is used in speech recognition. This structure is used with the <a href="/windows/desktop/api/ctffunc/nf-ctffunc-ienumtflatticeelements-next">IEnumTfLatticeElements::Next</a> method.

## -struct-fields

### -field dwFrameStart

Contains the starting offset, in 100-nanosecond units, of the element relative to the start of the phrase.

### -field dwFrameLen

Contains the length, in 100-nanosecond units, of the element.

### -field dwFlags

Not currently used.

### -field iCost

Specifies the actual confidence for this element. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SP_LOW_CONFIDENCE</td>
<td>The speech engine has low confidence in the element.</td>
</tr>
<tr>
<td>SP_NORMAL_CONFIDENCE</td>
<td>The speech engine has normal confidence in the element.</td>
</tr>
<tr>
<td>SP_HIGH_CONFIDENCE</td>
<td>The speech engine has high confidence in the element.</td>
</tr>
</table>

### -field bstrText

Contains the display text for the element. If the spoken word is "two", the display text will be "2". The caller must free this string using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

## -see-also

<a href="/windows/desktop/api/ctffunc/nf-ctffunc-ienumtflatticeelements-next">IEnumTfLatticeElements::Next
      </a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>