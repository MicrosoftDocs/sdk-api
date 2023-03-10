---
UID: NF:uianimation.IUIAnimationVariable.GetFinalValue
title: IUIAnimationVariable::GetFinalValue (uianimation.h)
description: Gets the final value of the animation variable. This is the value after all currently scheduled animations have completed. (IUIAnimationVariable.GetFinalValue)
helpviewer_keywords: ["GetFinalValue","GetFinalValue method [Windows Animation]","GetFinalValue method [Windows Animation]","IUIAnimationVariable interface","IUIAnimationVariable interface [Windows Animation]","GetFinalValue method","IUIAnimationVariable.GetFinalValue","IUIAnimationVariable::GetFinalValue","uianimation.iuianimationvariable_getfinalvalue","uianimation/IUIAnimationVariable::GetFinalValue"]
old-location: uianimation\iuianimationvariable_getfinalvalue.htm
tech.root: UIAnimation
ms.assetid: 577f83c1-aba7-4a51-82dc-68a103a31377
ms.date: 12/05/2018
ms.keywords: GetFinalValue, GetFinalValue method [Windows Animation], GetFinalValue method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetFinalValue method, IUIAnimationVariable.GetFinalValue, IUIAnimationVariable::GetFinalValue, uianimation.iuianimationvariable_getfinalvalue, uianimation/IUIAnimationVariable::GetFinalValue
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
 - IUIAnimationVariable::GetFinalValue
 - uianimation/IUIAnimationVariable::GetFinalValue
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
 - IUIAnimationVariable.GetFinalValue
---

# IUIAnimationVariable::GetFinalValue


## -description

Gets the final value of the animation variable.  
   This is the value after all currently scheduled animations have completed.

## -parameters

### -param finalValue [out]

The final value of the animation variable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_VALUE_NOT_DETERMINED</b></dt>
</dl>
</td>
<td width="60%">
The final value of the animation variable cannot be determined at this time.

</td>
</tr>
</table>

## -remarks

The result can be affected by the lower and upper bounds determined by <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a> and <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>, respectively.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalintegervalue">IUIAnimationVariable::GetFinalIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousvalue">IUIAnimationVariable::GetPreviousValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">IUIAnimationVariable::GetValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>
