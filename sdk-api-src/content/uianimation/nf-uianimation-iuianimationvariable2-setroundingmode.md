---
UID: NF:uianimation.IUIAnimationVariable2.SetRoundingMode
title: IUIAnimationVariable2::SetRoundingMode (uianimation.h)
description: Sets the rounding mode of the animation variable.
helpviewer_keywords: ["IUIAnimationVariable2 interface [Windows Animation]","SetRoundingMode method","IUIAnimationVariable2.SetRoundingMode","IUIAnimationVariable2::SetRoundingMode","SetRoundingMode","SetRoundingMode method [Windows Animation]","SetRoundingMode method [Windows Animation]","IUIAnimationVariable2 interface","uianimation.iuianimationvariable2_setroundingmode","uianimation/IUIAnimationVariable2::SetRoundingMode"]
old-location: uianimation\iuianimationvariable2_setroundingmode.htm
tech.root: UIAnimation
ms.assetid: D2FCC17B-0584-4317-8BD7-25454E4A553C
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetRoundingMode method, IUIAnimationVariable2.SetRoundingMode, IUIAnimationVariable2::SetRoundingMode, SetRoundingMode, SetRoundingMode method [Windows Animation], SetRoundingMode method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setroundingmode, uianimation/IUIAnimationVariable2::SetRoundingMode
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
 - IUIAnimationVariable2::SetRoundingMode
 - uianimation/IUIAnimationVariable2::SetRoundingMode
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
 - IUIAnimationVariable2.SetRoundingMode
---

# IUIAnimationVariable2::SetRoundingMode


## -description

Sets the rounding mode of the animation variable.

## -parameters

### -param mode [in]

The rounding mode.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

An animation variable's rounding mode determines how a floating-point value is converted to an integer.
      The default mode for each variable is <b>UI_ANIMATION_ROUNDING_NEAREST</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalintegervalue">IUIAnimationVariable2::GetFinalIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getintegervalue">IUIAnimationVariable2::GetIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousintegervalue">IUIAnimationVariable2::GetPreviousIntegerValue</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_rounding_mode">UI_ANIMATION_ROUNDING_MODE</a>