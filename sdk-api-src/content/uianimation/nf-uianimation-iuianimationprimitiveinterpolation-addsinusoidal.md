---
UID: NF:uianimation.IUIAnimationPrimitiveInterpolation.AddSinusoidal
title: IUIAnimationPrimitiveInterpolation::AddSinusoidal (uianimation.h)
description: Adds a sinusoidal segment that describes the shape of a transition curve to the animation function.
helpviewer_keywords: ["AddSinusoidal","AddSinusoidal method [Windows Animation]","AddSinusoidal method [Windows Animation]","IUIAnimationPrimitiveInterpolation interface","IUIAnimationPrimitiveInterpolation interface [Windows Animation]","AddSinusoidal method","IUIAnimationPrimitiveInterpolation.AddSinusoidal","IUIAnimationPrimitiveInterpolation::AddSinusoidal","uianimation.iuianimationprimitiveinterpolation_addsinusoidal","uianimation/IUIAnimationPrimitiveInterpolation::AddSinusoidal"]
old-location: uianimation\iuianimationprimitiveinterpolation_addsinusoidal.htm
tech.root: UIAnimation
ms.assetid: AF2BD96D-45A2-415B-A1BD-320C43F50360
ms.date: 12/05/2018
ms.keywords: AddSinusoidal, AddSinusoidal method [Windows Animation], AddSinusoidal method [Windows Animation],IUIAnimationPrimitiveInterpolation interface, IUIAnimationPrimitiveInterpolation interface [Windows Animation],AddSinusoidal method, IUIAnimationPrimitiveInterpolation.AddSinusoidal, IUIAnimationPrimitiveInterpolation::AddSinusoidal, uianimation.iuianimationprimitiveinterpolation_addsinusoidal, uianimation/IUIAnimationPrimitiveInterpolation::AddSinusoidal
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAnimation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationPrimitiveInterpolation::AddSinusoidal
 - uianimation/IUIAnimationPrimitiveInterpolation::AddSinusoidal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationPrimitiveInterpolation.AddSinusoidal
---

# IUIAnimationPrimitiveInterpolation::AddSinusoidal


## -description

Adds a sinusoidal segment that describes the shape of a transition curve to the animation function.

## -parameters

### -param dimension [in]

The dimension in which to apply the new segment.

### -param beginOffset [in]

The begin offset for the segment, where 0 corresponds to the start of the transition.

### -param bias [in]

The bias constant in the sinusoidal function.

### -param amplitude [in]

The amplitude constant in the sinusoidal function.

### -param frequency [in]

The frequency constant in the sinusoidal function.

### -param phase [in]

The phase constant in the sinusoidal function.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Defined by the function Y(t) = bias + amplitude*sin(360*frequency*t + phase), where 'sin' is the sin of an angle specified in degrees (for example, sin(n + 360) == sin(n) for any real number 'n').

This method will fail with an error code of UI_E_INVALID_PRIMITIVE if the start time is either less than 0
or less than the start time of  a previous segment.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprimitiveinterpolation">IUIAnimationPrimitiveInterpolation</a>