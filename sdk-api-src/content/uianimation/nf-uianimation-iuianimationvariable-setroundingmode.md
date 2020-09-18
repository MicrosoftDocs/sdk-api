---
UID: NF:uianimation.IUIAnimationVariable.SetRoundingMode
title: IUIAnimationVariable::SetRoundingMode (uianimation.h)
description: Specifies the rounding mode for the animation variable.
helpviewer_keywords: ["IUIAnimationVariable interface [Windows Animation]","SetRoundingMode method","IUIAnimationVariable.SetRoundingMode","IUIAnimationVariable::SetRoundingMode","SetRoundingMode","SetRoundingMode method [Windows Animation]","SetRoundingMode method [Windows Animation]","IUIAnimationVariable interface","uianimation.iuianimationvariable_setroundingmode","uianimation/IUIAnimationVariable::SetRoundingMode"]
old-location: uianimation\iuianimationvariable_setroundingmode.htm
tech.root: UIAnimation
ms.assetid: e8c86195-14a1-4535-9fc2-4992c8090e79
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetRoundingMode method, IUIAnimationVariable.SetRoundingMode, IUIAnimationVariable::SetRoundingMode, SetRoundingMode, SetRoundingMode method [Windows Animation], SetRoundingMode method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_setroundingmode, uianimation/IUIAnimationVariable::SetRoundingMode
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
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
 - IUIAnimationVariable::SetRoundingMode
 - uianimation/IUIAnimationVariable::SetRoundingMode
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
 - IUIAnimationVariable.SetRoundingMode
---

# IUIAnimationVariable::SetRoundingMode


## -description

Specifies the rounding mode for the animation variable.

## -parameters

### -param mode [in]

The rounding mode for the animation variable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

An animation variable's rounding mode determines how a floating-point value is converted to an integer.
      The default mode for each variable is <b>UI_ANIMATION_ROUNDING_NEAREST</b>.


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/create-animation-variables">Create Animation Variables</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalintegervalue">IUIAnimationVariable::GetFinalIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_rounding_mode">UI_ANIMATION_ROUNDING_MODE</a>