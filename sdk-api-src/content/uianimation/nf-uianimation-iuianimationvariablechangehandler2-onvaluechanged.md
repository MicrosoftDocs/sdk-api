---
UID: NF:uianimation.IUIAnimationVariableChangeHandler2.OnValueChanged
title: IUIAnimationVariableChangeHandler2::OnValueChanged (uianimation.h)
description: Handles events that occur when the value of an animation variable changes in the specified dimension.
helpviewer_keywords: ["IUIAnimationVariableChangeHandler2 interface [Windows Animation]","OnValueChanged method","IUIAnimationVariableChangeHandler2.OnValueChanged","IUIAnimationVariableChangeHandler2::OnValueChanged","OnValueChanged","OnValueChanged method [Windows Animation]","OnValueChanged method [Windows Animation]","IUIAnimationVariableChangeHandler2 interface","uianimation.iuianimationvariablechangehandler2_onvaluechanged","uianimation/IUIAnimationVariableChangeHandler2::OnValueChanged"]
old-location: uianimation\iuianimationvariablechangehandler2_onvaluechanged.htm
tech.root: UIAnimation
ms.assetid: 3C885518-8EAC-4123-83A5-5DEB27523DEF
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableChangeHandler2 interface [Windows Animation],OnValueChanged method, IUIAnimationVariableChangeHandler2.OnValueChanged, IUIAnimationVariableChangeHandler2::OnValueChanged, OnValueChanged, OnValueChanged method [Windows Animation], OnValueChanged method [Windows Animation],IUIAnimationVariableChangeHandler2 interface, uianimation.iuianimationvariablechangehandler2_onvaluechanged, uianimation/IUIAnimationVariableChangeHandler2::OnValueChanged
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
 - IUIAnimationVariableChangeHandler2::OnValueChanged
 - uianimation/IUIAnimationVariableChangeHandler2::OnValueChanged
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
 - IUIAnimationVariableChangeHandler2.OnValueChanged
---

# IUIAnimationVariableChangeHandler2::OnValueChanged


## -description

Handles events that occur when the value of an animation variable changes in the specified dimension.

## -parameters

### -param storyboard [in]

The storyboard that is animating the animation variable specified by the <i>variable</i> parameter.

### -param variable [in]

The animation variable that has been updated.

### -param newValue [in]

The new value of the animation variable.

### -param previousValue [in]

The previous value of the animation variable.

### -param cDimension [in]

The dimension in which the value of the animation variable changed.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method receives updates as <b>DOUBLE</b> values.  
         To receive updates as <b>INT32</b> values, use the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler2-onintegervaluechanged">IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged</a> method.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>IUIAnimationVariableChangeHandler2::OnValueChanged</b>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getvalue">IUIAnimationVariable2::GetValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalvalue">IUIAnimationVariable2::GetFinalValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousvalue">IUIAnimationVariable2::GetPreviousValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getintegervalue">IUIAnimationVariable2::GetIntegerValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalintegervalue">IUIAnimationVariable2::GetFinalIntegerValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousintegervalue">IUIAnimationVariable2::GetPreviousIntegerValue
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurrentstoryboard">IUIAnimationVariable2::GetCurrentStoryboard
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-gettag">IUIAnimationVariable2::GetTag
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getvariablefromtag">IUIAnimationManager2::GetVariableFromTag
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstoryboardfromtag">IUIAnimationManager2::GetStoryboardFromTag
</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-gettag">IUIAnimationStoryboard2::GetTag
</a>
</li>
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
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-gettag">IUIAnimationVariable::GetTag
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
</ul>

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setvariablechangehandler">IUIAnimationVariable2::SetVariableChangeHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariablechangehandler2">IUIAnimationVariableChangeHandler2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariableintegerchangehandler2">IUIAnimationVariableIntegerChangeHandler2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler2-onintegervaluechanged">IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged</a>