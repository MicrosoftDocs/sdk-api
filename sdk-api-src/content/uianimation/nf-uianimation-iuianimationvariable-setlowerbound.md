---
UID: NF:uianimation.IUIAnimationVariable.SetLowerBound
title: IUIAnimationVariable::SetLowerBound (uianimation.h)
description: Sets the lower bound (floor) for the animation variable. The value of the animation variable should not fall below the specified value.
helpviewer_keywords: ["IUIAnimationVariable interface [Windows Animation]","SetLowerBound method","IUIAnimationVariable.SetLowerBound","IUIAnimationVariable::SetLowerBound","SetLowerBound","SetLowerBound method [Windows Animation]","SetLowerBound method [Windows Animation]","IUIAnimationVariable interface","uianimation.iuianimationvariable_setlowerbound","uianimation/IUIAnimationVariable::SetLowerBound"]
old-location: uianimation\iuianimationvariable_setlowerbound.htm
tech.root: UIAnimation
ms.assetid: 1e8f1106-6320-4670-867a-24ce6597026e
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetLowerBound method, IUIAnimationVariable.SetLowerBound, IUIAnimationVariable::SetLowerBound, SetLowerBound, SetLowerBound method [Windows Animation], SetLowerBound method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_setlowerbound, uianimation/IUIAnimationVariable::SetLowerBound
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
 - IUIAnimationVariable::SetLowerBound
 - uianimation/IUIAnimationVariable::SetLowerBound
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
 - IUIAnimationVariable.SetLowerBound
---

# IUIAnimationVariable::SetLowerBound


## -description

Sets the lower bound (floor) for the animation variable. The value of the animation variable should not fall below the specified value.

## -parameters

### -param bound [in]

The lower bound for the animation variable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalintegervalue">IUIAnimationVariable::GetFinalIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalvalue">IUIAnimationVariable::GetFinalValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousvalue">IUIAnimationVariable::GetPreviousValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">IUIAnimationVariable::GetValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>