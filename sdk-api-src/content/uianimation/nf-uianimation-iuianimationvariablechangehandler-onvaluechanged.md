---
UID: NF:uianimation.IUIAnimationVariableChangeHandler.OnValueChanged
title: IUIAnimationVariableChangeHandler::OnValueChanged (uianimation.h)
description: Handles events that occur when the value of an animation variable changes. (IUIAnimationVariableChangeHandler.OnValueChanged)
helpviewer_keywords: ["IUIAnimationVariableChangeHandler interface [Windows Animation]","OnValueChanged method","IUIAnimationVariableChangeHandler.OnValueChanged","IUIAnimationVariableChangeHandler::OnValueChanged","OnValueChanged","OnValueChanged method [Windows Animation]","OnValueChanged method [Windows Animation]","IUIAnimationVariableChangeHandler interface","uianimation.iuianimationvariablechangehandler_onvaluechanged","uianimation/IUIAnimationVariableChangeHandler::OnValueChanged"]
old-location: uianimation\iuianimationvariablechangehandler_onvaluechanged.htm
tech.root: UIAnimation
ms.assetid: 1e865f55-d703-4d91-8690-b816b5fe1a89
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableChangeHandler interface [Windows Animation],OnValueChanged method, IUIAnimationVariableChangeHandler.OnValueChanged, IUIAnimationVariableChangeHandler::OnValueChanged, OnValueChanged, OnValueChanged method [Windows Animation], OnValueChanged method [Windows Animation],IUIAnimationVariableChangeHandler interface, uianimation.iuianimationvariablechangehandler_onvaluechanged, uianimation/IUIAnimationVariableChangeHandler::OnValueChanged
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
 - IUIAnimationVariableChangeHandler::OnValueChanged
 - uianimation/IUIAnimationVariableChangeHandler::OnValueChanged
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
 - IUIAnimationVariableChangeHandler.OnValueChanged
---

# IUIAnimationVariableChangeHandler::OnValueChanged


## -description

Handles events that occur when the value of an animation variable changes.

This method receives updates as <b>DOUBLE</b> values.  
         To receive updates as <b>INT32</b> values, use the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged">IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged</a> method.

## -parameters

### -param storyboard [in]

The storyboard that is animating the animation variable specified by the <i>variable</i> parameter.

### -param variable [in]

The animation variable that has been updated.

### -param newValue [in]

The new value of the animation variable.

### -param previousValue [in]

The previous value of the animation variable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnValueChanged</b>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">IUIAnimationVariable::GetValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalvalue">IUIAnimationVariable::GetFinalValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousvalue">IUIAnimationVariable::GetPreviousValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalintegervalue">IUIAnimationVariable::GetFinalIntegerValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">IUIAnimationVariable::GetPreviousIntegerValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getcurrentstoryboard">IUIAnimationVariable::GetCurrentStoryboard
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getvariablefromtag">IUIAnimationManager::GetVariableFromTag
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstoryboardfromtag">IUIAnimationManager::GetStoryboardFromTag
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-gettag">IUIAnimationStoryboard::GetTag
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-gettag">IUIAnimationVariable::GetTag
</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousvalue">IUIAnimationVariable::GetPreviousValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">IUIAnimationVariable::GetValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariablechangehandler">IUIAnimationVariable::SetVariableChangeHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariablechangehandler">IUIAnimationVariableChangeHandler</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged">IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged</a>
