---
UID: NF:uianimation.IUIAnimationVariable.SetUpperBound
title: IUIAnimationVariable::SetUpperBound (uianimation.h)
description: Sets an upper bound (ceiling) for the animation variable. The value of the animation variable should not rise above the specified value.
helpviewer_keywords: ["IUIAnimationVariable interface [Windows Animation]","SetUpperBound method","IUIAnimationVariable.SetUpperBound","IUIAnimationVariable::SetUpperBound","SetUpperBound","SetUpperBound method [Windows Animation]","SetUpperBound method [Windows Animation]","IUIAnimationVariable interface","uianimation.iuianimationvariable_setupperbound","uianimation/IUIAnimationVariable::SetUpperBound"]
old-location: uianimation\iuianimationvariable_setupperbound.htm
tech.root: UIAnimation
ms.assetid: d202f453-2e69-415b-823c-5a3279722274
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetUpperBound method, IUIAnimationVariable.SetUpperBound, IUIAnimationVariable::SetUpperBound, SetUpperBound, SetUpperBound method [Windows Animation], SetUpperBound method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_setupperbound, uianimation/IUIAnimationVariable::SetUpperBound
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
 - IUIAnimationVariable::SetUpperBound
 - uianimation/IUIAnimationVariable::SetUpperBound
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
 - IUIAnimationVariable.SetUpperBound
---

# IUIAnimationVariable::SetUpperBound


## -description

Sets an upper bound (ceiling) for the animation variable. The value of the animation variable should not rise above the specified value.

## -parameters

### -param bound [in]

The upper bound for the animation variable.

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



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a>