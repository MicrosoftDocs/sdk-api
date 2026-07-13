---
UID: NF:dcomp.IDCompositionBrightnessEffect.SetWhitePoint
title: IDCompositionBrightnessEffect::SetWhitePoint (dcomp.h)
description: Sets the upper portion of the brightness transfer curve.
helpviewer_keywords: ["IDCompositionBrightnessEffect interface [DirectComposition]","SetWhitePoint method","IDCompositionBrightnessEffect.SetWhitePoint","IDCompositionBrightnessEffect::SetWhitePoint","SetWhitePoint","SetWhitePoint method [DirectComposition]","SetWhitePoint method [DirectComposition]","IDCompositionBrightnessEffect interface","dcomp/IDCompositionBrightnessEffect::SetWhitePoint","directcomp.idcompositionbrightnesseffect_setwhitepoint"]
old-location: directcomp\idcompositionbrightnesseffect_setwhitepoint.htm
tech.root: directcomp
ms.assetid: C06DFD2A-9B97-4254-BFB5-058FB0ED3F83
ms.date: 12/05/2018
ms.keywords: IDCompositionBrightnessEffect interface [DirectComposition],SetWhitePoint method, IDCompositionBrightnessEffect.SetWhitePoint, IDCompositionBrightnessEffect::SetWhitePoint, SetWhitePoint, SetWhitePoint method [DirectComposition], SetWhitePoint method [DirectComposition],IDCompositionBrightnessEffect interface, dcomp/IDCompositionBrightnessEffect::SetWhitePoint, directcomp.idcompositionbrightnesseffect_setwhitepoint
req.header: dcomp.h
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionBrightnessEffect::SetWhitePoint
 - dcomp/IDCompositionBrightnessEffect::SetWhitePoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionBrightnessEffect.SetWhitePoint
---

# IDCompositionBrightnessEffect::SetWhitePoint


## -description

Sets the upper portion of the brightness transfer curve.

## -parameters

### -param whitePoint [in, ref]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a></b>

The upper portion of the brightness transfer curve. The white point adjusts the appearance of the brighter portions of the image. 
This vector is for both the x value and the y value, in that order. Each of the values must be between 0 and 1, inclusive.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionbrightnesseffect">IDCompositionBrightnessEffect</a>