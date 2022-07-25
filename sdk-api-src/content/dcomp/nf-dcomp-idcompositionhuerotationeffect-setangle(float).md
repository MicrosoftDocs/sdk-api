---
UID: NF:dcomp.IDCompositionHueRotationEffect.SetAngle(float)
title: IDCompositionHueRotationEffect::SetAngle(float) (dcomp.h)
description: The IDCompositionHueRotationEffect::SetAngle(float) method sets the angle to rotate the hue.
helpviewer_keywords: ["IDCompositionHueRotationEffect interface [DirectComposition]","SetAngle method","IDCompositionHueRotationEffect.SetAngle","IDCompositionHueRotationEffect.SetAngle(float)","IDCompositionHueRotationEffect::SetAngle","IDCompositionHueRotationEffect::SetAngle(float)","SetAngle","SetAngle method [DirectComposition]","SetAngle method [DirectComposition]","IDCompositionHueRotationEffect interface","dcomp/IDCompositionHueRotationEffect::SetAngle","directcomp.idcompositionhuerotationeffect_setangle"]
old-location: directcomp\idcompositionhuerotationeffect_setangle.htm
tech.root: directcomp
ms.assetid: BA98A918-EE51-40C7-9392-D5E0D78580F8
ms.date: 06/23/2022
ms.keywords: IDCompositionHueRotationEffect interface [DirectComposition],SetAngle method, IDCompositionHueRotationEffect.SetAngle, IDCompositionHueRotationEffect.SetAngle(float), IDCompositionHueRotationEffect::SetAngle, IDCompositionHueRotationEffect::SetAngle(float), SetAngle, SetAngle method [DirectComposition], SetAngle method [DirectComposition],IDCompositionHueRotationEffect interface, dcomp/IDCompositionHueRotationEffect::SetAngle, directcomp.idcompositionhuerotationeffect_setangle
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
 - IDCompositionHueRotationEffect::SetAngle
 - dcomp/IDCompositionHueRotationEffect::SetAngle
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
 - IDCompositionHueRotationEffect.SetAngle
---

# IDCompositionHueRotationEffect::SetAngle(float)


## -description

Sets the angle to rotate the hue.

## -parameters

### -param amountDegrees [in]

Type: <b>float</b>

The angle to rotate the hue. The effect calculates a color matrix based on the rotation angle (θ) according to the following matrix equations:
          

<img alt="Matrix equation" src="./images/hue_formula.png"/>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionhuerotationeffect">IDCompositionHueRotationEffect</a>