---
UID: NF:uianimation.IUIAnimationVariable.GetPreviousValue
title: IUIAnimationVariable::GetPreviousValue (uianimation.h)
description: Gets the previous value of the animation variable. This is the value of the animation variable before the most recent update. (IUIAnimationVariable.GetPreviousValue)
helpviewer_keywords: ["GetPreviousValue","GetPreviousValue method [Windows Animation]","GetPreviousValue method [Windows Animation]","IUIAnimationVariable interface","IUIAnimationVariable interface [Windows Animation]","GetPreviousValue method","IUIAnimationVariable.GetPreviousValue","IUIAnimationVariable::GetPreviousValue","uianimation.iuianimationvariable_getpreviousvalue","uianimation/IUIAnimationVariable::GetPreviousValue"]
old-location: uianimation\iuianimationvariable_getpreviousvalue.htm
tech.root: UIAnimation
ms.assetid: 405bc35e-8b38-40fb-acf4-107fa6dd161a
ms.date: 12/05/2018
ms.keywords: GetPreviousValue, GetPreviousValue method [Windows Animation], GetPreviousValue method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetPreviousValue method, IUIAnimationVariable.GetPreviousValue, IUIAnimationVariable::GetPreviousValue, uianimation.iuianimationvariable_getpreviousvalue, uianimation/IUIAnimationVariable::GetPreviousValue
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
 - IUIAnimationVariable::GetPreviousValue
 - uianimation/IUIAnimationVariable::GetPreviousValue
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
 - IUIAnimationVariable.GetPreviousValue
---

# IUIAnimationVariable::GetPreviousValue


## -description

Gets the previous value of the animation variable. This is the value of the animation variable before the most recent update.

## -parameters

### -param previousValue [out]

The previous value of the animation variable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The results can be affected by the lower and upper bounds determined by <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a> and <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>, respectively.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalvalue">IUIAnimationVariable::GetFinalValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>
