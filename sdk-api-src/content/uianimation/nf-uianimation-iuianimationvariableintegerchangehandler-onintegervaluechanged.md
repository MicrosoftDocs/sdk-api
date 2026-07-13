---
UID: NF:uianimation.IUIAnimationVariableIntegerChangeHandler.OnIntegerValueChanged
title: IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged (uianimation.h)
description: Handles events that occur when the value of an animation variable changes. (IUIAnimationVariableIntegerChangeHandler.OnIntegerValueChanged)
helpviewer_keywords: ["IUIAnimationVariableIntegerChangeHandler interface [Windows Animation]","OnIntegerValueChanged method","IUIAnimationVariableIntegerChangeHandler.OnIntegerValueChanged","IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged","OnIntegerValueChanged","OnIntegerValueChanged method [Windows Animation]","OnIntegerValueChanged method [Windows Animation]","IUIAnimationVariableIntegerChangeHandler interface","uianimation.iuianimationvariableintegerchangehandler_onintegervaluechanged","uianimation/IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged"]
old-location: uianimation\iuianimationvariableintegerchangehandler_onintegervaluechanged.htm
tech.root: UIAnimation
ms.assetid: e12224a2-c8f3-45eb-a254-d624de16e12d
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableIntegerChangeHandler interface [Windows Animation],OnIntegerValueChanged method, IUIAnimationVariableIntegerChangeHandler.OnIntegerValueChanged, IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged, OnIntegerValueChanged, OnIntegerValueChanged method [Windows Animation], OnIntegerValueChanged method [Windows Animation],IUIAnimationVariableIntegerChangeHandler interface, uianimation.iuianimationvariableintegerchangehandler_onintegervaluechanged, uianimation/IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged
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
 - IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged
 - uianimation/IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged
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
 - IUIAnimationVariableIntegerChangeHandler.OnIntegerValueChanged
---

# IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged


## -description

Handles events that occur when the value of an animation variable changes.

This method receives updates as <b>INT32</b> values. To receive updates as <b>DOUBLE</b> values, use the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged">IUIAnimationVariableChangeHandler::OnValueChanged</a> method.

## -parameters

### -param storyboard [in]

The storyboard that is animating the animation variable  specified by the <i>variable</i> parameter.

### -param variable [in]

The animation variable that has been updated.

### -param newValue [in]

The new value of the animation variable, rounded according to the variable's rounding mode.

### -param previousValue [in]

The previous value of the animation variable, rounded according to the variable's rounding mode.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The rounding mode for an animation variable is specified using the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setroundingmode">IUIAnimationVariable::SetRoundingMode</a> method.

<b>OnIntegerValueChanged</b> events might occur less frequently than <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged">OnValueChanged</a> events because values such as 2.2, 2.3, 2.4 would all be rounded to the same integer.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnIntegerValueChanged</b>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getcurrentstoryboard">IUIAnimationVariable::GetCurrentStoryboard</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalintegervalue">IUIAnimationVariable::GetFinalIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalvalue">IUIAnimationVariable::GetFinalValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">IUIAnimationVariable::GetPreviousIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousvalue">IUIAnimationVariable::GetPreviousValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">IUIAnimationVariable::GetValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstoryboardfromtag">IUIAnimationManager::GetStoryboardFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getvariablefromtag">IUIAnimationManager::GetVariableFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-gettag">IUIAnimationStoryboard::GetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-gettag">IUIAnimationVariable::GetTag</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setroundingmode">IUIAnimationVariable::SetRoundingMode</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler">IUIAnimationVariable::SetVariableIntegerChangeHandler</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged">IUIAnimationVariableChangeHandler::OnValueChanged</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariableintegerchangehandler">IUIAnimationVariableIntegerChangeHandler</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_rounding_mode">UI_ANIMATION_ROUNDING_MODE </a>
