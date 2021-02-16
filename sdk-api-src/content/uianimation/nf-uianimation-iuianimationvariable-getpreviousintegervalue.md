---
UID: NF:uianimation.IUIAnimationVariable.GetPreviousIntegerValue
title: IUIAnimationVariable::GetPreviousIntegerValue (uianimation.h)
description: Gets the previous value of the animation variable as an integer. This is the value of the animation variable before the most recent update.
helpviewer_keywords: ["GetPreviousIntegerValue","GetPreviousIntegerValue method [Windows Animation]","GetPreviousIntegerValue method [Windows Animation]","IUIAnimationVariable interface","IUIAnimationVariable interface [Windows Animation]","GetPreviousIntegerValue method","IUIAnimationVariable.GetPreviousIntegerValue","IUIAnimationVariable::GetPreviousIntegerValue","uianimation.iuianimationvariable_getpreviousintegervalue","uianimation/IUIAnimationVariable::GetPreviousIntegerValue"]
old-location: uianimation\iuianimationvariable_getpreviousintegervalue.htm
tech.root: UIAnimation
ms.assetid: ccf4c575-aa98-40cd-b2de-cf8db95ec57d
ms.date: 12/05/2018
ms.keywords: GetPreviousIntegerValue, GetPreviousIntegerValue method [Windows Animation], GetPreviousIntegerValue method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetPreviousIntegerValue method, IUIAnimationVariable.GetPreviousIntegerValue, IUIAnimationVariable::GetPreviousIntegerValue, uianimation.iuianimationvariable_getpreviousintegervalue, uianimation/IUIAnimationVariable::GetPreviousIntegerValue
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
 - IUIAnimationVariable::GetPreviousIntegerValue
 - uianimation/IUIAnimationVariable::GetPreviousIntegerValue
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
 - IUIAnimationVariable.GetPreviousIntegerValue
---

# IUIAnimationVariable::GetPreviousIntegerValue


## -description

Gets the previous value of the animation variable as an integer.      
   This is the value of the animation variable before the most recent update.

## -parameters

### -param previousValue [out]

The previous value of the animation variable, converted to an <b>INT32</b> value.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

To specify the rounding mode to be used when converting the value, use the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setroundingmode">IUIAnimationVariable::SetRoundingMode</a> method.

The result can also be affected by the lower and upper bounds determined by <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a> and <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>, respectively.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalintegervalue">IUIAnimationVariable::GetFinalIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousvalue">IUIAnimationVariable::GetPreviousValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setroundingmode">IUIAnimationVariable::SetRoundingMode</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>