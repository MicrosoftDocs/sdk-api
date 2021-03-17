---
UID: NF:mfapi.MFllMulDiv
title: MFllMulDiv function (mfapi.h)
description: Calculates ((a * b) + d) / c, where each term is a 64-bit signed value.
helpviewer_keywords: ["MFllMulDiv","MFllMulDiv function [Media Foundation]","mf.mfllmuldiv","mfapi/MFllMulDiv"]
old-location: mf\mfllmuldiv.htm
tech.root: mf
ms.assetid: ee369c2e-99a1-4ee4-ac67-02f14e11e269
ms.date: 12/05/2018
ms.keywords: MFllMulDiv, MFllMulDiv function [Media Foundation], mf.mfllmuldiv, mfapi/MFllMulDiv
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFllMulDiv
 - mfapi/MFllMulDiv
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFllMulDiv
---

# MFllMulDiv function


## -description

Calculates ((a * b) + d) / c, where each term is a 64-bit signed value.

## -parameters

### -param a

A multiplier.

### -param b

Another multiplier.

### -param c

The divisor.

### -param d

The rounding factor.

## -returns

Returns the result of the calculation. If numeric overflow occurs, the function returns _I64_MAX (positive overflow) or LLONG_MIN (negative overflow). If Mfplat.dll cannot be loaded, the function returns _I64_MAX.

## -remarks

<div class="alert"><b>Note</b>  A previous version of this topic described the parameters incorrectly. The divisor is <i>c</i> and the rounding factor is <i>d</i>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>