---
UID: NF:uianimation.IUIAnimationVariable.GetIntegerValue
title: IUIAnimationVariable::GetIntegerValue (uianimation.h)
description: Gets the current value of the animation variable as an integer.
helpviewer_keywords: ["GetIntegerValue","GetIntegerValue method [Windows Animation]","GetIntegerValue method [Windows Animation]","IUIAnimationVariable interface","IUIAnimationVariable interface [Windows Animation]","GetIntegerValue method","IUIAnimationVariable.GetIntegerValue","IUIAnimationVariable::GetIntegerValue","uianimation.iuianimationvariable_getintegervalue","uianimation/IUIAnimationVariable::GetIntegerValue"]
old-location: uianimation\iuianimationvariable_getintegervalue.htm
tech.root: UIAnimation
ms.assetid: 044fd6a3-6e40-4f4f-8777-1a1a66c91989
ms.date: 12/05/2018
ms.keywords: GetIntegerValue, GetIntegerValue method [Windows Animation], GetIntegerValue method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetIntegerValue method, IUIAnimationVariable.GetIntegerValue, IUIAnimationVariable::GetIntegerValue, uianimation.iuianimationvariable_getintegervalue, uianimation/IUIAnimationVariable::GetIntegerValue
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
 - IUIAnimationVariable::GetIntegerValue
 - uianimation/IUIAnimationVariable::GetIntegerValue
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
 - IUIAnimationVariable.GetIntegerValue
---

# IUIAnimationVariable::GetIntegerValue


## -description

Gets the current value of the animation variable as an integer.

## -parameters

### -param value [out]

The current value of the animation variable, converted to an <b>INT32</b> value.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

To specify the rounding mode to be used when converting the value, use the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setroundingmode">IUIAnimationVariable::SetRoundingMode</a> method.

The result can also be affected by the lower and upper bounds determined by <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a> and <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>, respectively.


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/updating---application-driven-animation">Read the Animation Variable Values</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalintegervalue">IUIAnimationVariable::GetFinalIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">IUIAnimationVariable::GetValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setroundingmode">IUIAnimationVariable::SetRoundingMode</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>