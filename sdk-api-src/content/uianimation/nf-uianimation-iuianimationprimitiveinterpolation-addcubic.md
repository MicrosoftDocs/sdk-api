---
UID: NF:uianimation.IUIAnimationPrimitiveInterpolation.AddCubic
title: IUIAnimationPrimitiveInterpolation::AddCubic (uianimation.h)
description: Adds a cubic polynomial segment that describes the shape of a transition curve to the animation function.
helpviewer_keywords: ["AddCubic","AddCubic method [Windows Animation]","AddCubic method [Windows Animation]","IUIAnimationPrimitiveInterpolation interface","IUIAnimationPrimitiveInterpolation interface [Windows Animation]","AddCubic method","IUIAnimationPrimitiveInterpolation.AddCubic","IUIAnimationPrimitiveInterpolation::AddCubic","uianimation.iuianimationprimitiveinterpolation_addcubic","uianimation/IUIAnimationPrimitiveInterpolation::AddCubic"]
old-location: uianimation\iuianimationprimitiveinterpolation_addcubic.htm
tech.root: UIAnimation
ms.assetid: 98738F6A-364E-491F-BCA3-F8B74B036D89
ms.date: 12/05/2018
ms.keywords: AddCubic, AddCubic method [Windows Animation], AddCubic method [Windows Animation],IUIAnimationPrimitiveInterpolation interface, IUIAnimationPrimitiveInterpolation interface [Windows Animation],AddCubic method, IUIAnimationPrimitiveInterpolation.AddCubic, IUIAnimationPrimitiveInterpolation::AddCubic, uianimation.iuianimationprimitiveinterpolation_addcubic, uianimation/IUIAnimationPrimitiveInterpolation::AddCubic
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
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
 - IUIAnimationPrimitiveInterpolation::AddCubic
 - uianimation/IUIAnimationPrimitiveInterpolation::AddCubic
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
 - IUIAnimationPrimitiveInterpolation.AddCubic
---

# IUIAnimationPrimitiveInterpolation::AddCubic


## -description

Adds a cubic polynomial segment that describes the shape of a transition curve to the animation function.

## -parameters

### -param dimension [in]

The dimension in which to apply the new segment.

### -param beginOffset [in]

The begin offset for the segment, where 0 corresponds to the start of the transition.

### -param constantCoefficient [in]

The cubic polynomial constant coefficient.

### -param linearCoefficient [in]

The cubic polynomial linear coefficient.

### -param quadraticCoefficient [in]

The cubic polynomial quadratic coefficient.

### -param cubicCoefficient [in]

The cubic polynomial cubic coefficient.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method will fail with an error code of UI_E_INVALID_PRIMITIVE if the start time is either less than 0
or less than the start time of  a previous segment.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprimitiveinterpolation">IUIAnimationPrimitiveInterpolation</a>