---
UID: NF:uianimation.IUIAnimationVariable.GetValue
title: IUIAnimationVariable::GetValue (uianimation.h)
description: Gets the current value of the animation variable.
helpviewer_keywords: ["GetValue","GetValue method [Windows Animation]","GetValue method [Windows Animation]","IUIAnimationVariable interface","IUIAnimationVariable interface [Windows Animation]","GetValue method","IUIAnimationVariable.GetValue","IUIAnimationVariable::GetValue","uianimation.iuianimationvariable_getvalue","uianimation/IUIAnimationVariable::GetValue"]
old-location: uianimation\iuianimationvariable_getvalue.htm
tech.root: UIAnimation
ms.assetid: 51ae200a-a630-44fd-afd4-33d1b1dbf6d7
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Windows Animation], GetValue method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetValue method, IUIAnimationVariable.GetValue, IUIAnimationVariable::GetValue, uianimation.iuianimationvariable_getvalue, uianimation/IUIAnimationVariable::GetValue
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
 - IUIAnimationVariable::GetValue
 - uianimation/IUIAnimationVariable::GetValue
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
 - IUIAnimationVariable.GetValue
---

# IUIAnimationVariable::GetValue


## -description

Gets the current value of the animation variable.

## -parameters

### -param value [out]

The current value of the animation variable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The results can be affected by the lower and upper bounds determined by <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a> and <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>, respectively.


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/updating---application-driven-animation">Read the Animation Variable Values</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalvalue">IUIAnimationVariable::GetFinalValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousvalue">IUIAnimationVariable::GetPreviousValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>