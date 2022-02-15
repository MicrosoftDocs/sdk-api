---
UID: NF:dcomp.IDCompositionBrightnessEffect.SetBlackPoint
title: IDCompositionBrightnessEffect::SetBlackPoint (dcomp.h)
description: Specifies the lower portion of the brightness transfer curve for the brightness effect.
helpviewer_keywords: ["IDCompositionBrightnessEffect interface [DirectComposition]","SetBlackPoint method","IDCompositionBrightnessEffect.SetBlackPoint","IDCompositionBrightnessEffect::SetBlackPoint","SetBlackPoint","SetBlackPoint method [DirectComposition]","SetBlackPoint method [DirectComposition]","IDCompositionBrightnessEffect interface","dcomp/IDCompositionBrightnessEffect::SetBlackPoint","directcomp.idcompositionbrightnesseffect_setblackpoint"]
old-location: directcomp\idcompositionbrightnesseffect_setblackpoint.htm
tech.root: directcomp
ms.assetid: C63F0F4C-6C25-495A-8AD8-F1A453E0B4BA
ms.date: 12/05/2018
ms.keywords: IDCompositionBrightnessEffect interface [DirectComposition],SetBlackPoint method, IDCompositionBrightnessEffect.SetBlackPoint, IDCompositionBrightnessEffect::SetBlackPoint, SetBlackPoint, SetBlackPoint method [DirectComposition], SetBlackPoint method [DirectComposition],IDCompositionBrightnessEffect interface, dcomp/IDCompositionBrightnessEffect::SetBlackPoint, directcomp.idcompositionbrightnesseffect_setblackpoint
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
 - IDCompositionBrightnessEffect::SetBlackPoint
 - dcomp/IDCompositionBrightnessEffect::SetBlackPoint
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
 - IDCompositionBrightnessEffect.SetBlackPoint
---

# IDCompositionBrightnessEffect::SetBlackPoint


## -description

Specifies the lower portion of the brightness transfer curve for the brightness effect.

## -parameters

### -param blackPoint [in, ref]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a></b>

The lower portion of the brightness transfer curve. The black point adjusts the appearance of the darker portions of the image. The vector is for both the x value and the y value, in that order. Each of the values must be between 0 and 1, inclusive.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionbrightnesseffect">IDCompositionBrightnessEffect</a>