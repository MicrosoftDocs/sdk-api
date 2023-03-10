---
UID: NF:uianimation.IUIAnimationVariableIntegerChangeHandler2.OnIntegerValueChanged
title: IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged (uianimation.h)
description: Handles events that occur when the integer value of an animation variable changes in the specified dimension.
helpviewer_keywords: ["IUIAnimationVariableIntegerChangeHandler2 interface [Windows Animation]","OnIntegerValueChanged method","IUIAnimationVariableIntegerChangeHandler2.OnIntegerValueChanged","IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged","OnIntegerValueChanged","OnIntegerValueChanged method [Windows Animation]","OnIntegerValueChanged method [Windows Animation]","IUIAnimationVariableIntegerChangeHandler2 interface","uianimation.iuianimationvariableintegerchangehandler2_onintegervaluechanged","uianimation/IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged"]
old-location: uianimation\iuianimationvariableintegerchangehandler2_onintegervaluechanged.htm
tech.root: UIAnimation
ms.assetid: 76889784-BF1B-475B-8D84-201BEE6F0594
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableIntegerChangeHandler2 interface [Windows Animation],OnIntegerValueChanged method, IUIAnimationVariableIntegerChangeHandler2.OnIntegerValueChanged, IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged, OnIntegerValueChanged, OnIntegerValueChanged method [Windows Animation], OnIntegerValueChanged method [Windows Animation],IUIAnimationVariableIntegerChangeHandler2 interface, uianimation.iuianimationvariableintegerchangehandler2_onintegervaluechanged, uianimation/IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged
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
 - IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged
 - uianimation/IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged
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
 - IUIAnimationVariableIntegerChangeHandler2.OnIntegerValueChanged
---

# IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged


## -description

Handles events that occur when the integer value of an animation variable changes in the specified dimension.

## -parameters

### -param storyboard [in]

The storyboard that is animating the animation variable specified by the <i>variable</i> parameter.

### -param variable [in]

The animation variable that has been updated.

### -param newValue [in]

The new integer value of the animation variable.

<div class="alert"><b>Note</b>  The rounding mode for an animation variable is specified using the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setroundingmode">SetRoundingMode</a> method.</div>
<div> </div>

### -param previousValue [in]

The previous integer value of the animation variable.

<div class="alert"><b>Note</b>  The rounding mode for an animation variable is specified using the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setroundingmode">SetRoundingMode</a> method.</div>
<div> </div>

### -param cDimension [in]

The dimension in which the integer value of the animation variable changed.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method receives updates as <b>INT32</b> values.  
         To receive updates as <b>DOUBLE</b> values, use the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler2-onvaluechanged">OnValueChanged</a> method.

<b>OnIntegerValueChanged</b> events might occur less frequently than <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler2-onvaluechanged">OnValueChanged</a> events because values such as 2.2, 2.3, and 2.4 would all be rounded to the same integer.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnIntegerValueChanged</b>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getvalue">GetValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalvalue">GetFinalValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousvalue">GetPreviousValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getintegervalue">GetIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalintegervalue">GetFinalIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousintegervalue">GetPreviousIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurrentstoryboard">GetCurrentStoryboard</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getvariablefromtag">GetVariableFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstoryboardfromtag">GetStoryboardFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-gettag">GetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-gettag">GetTag</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariablechangehandler2">IUIAnimationVariableChangeHandler2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariableintegerchangehandler2">IUIAnimationVariableIntegerChangeHandler2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler2-onvaluechanged">OnValueChanged</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setvariableintegerchangehandler">SetVariableIntegerChangeHandler</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_rounding_mode">UI_ANIMATION_ROUNDING_MODE</a>