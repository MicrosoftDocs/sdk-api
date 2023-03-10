---
UID: NF:uianimation.IUIAnimationVariable.GetFinalIntegerValue
title: IUIAnimationVariable::GetFinalIntegerValue (uianimation.h)
description: Gets the final value of the animation variable as an integer. This is the value after all currently scheduled animations have completed.
helpviewer_keywords: ["GetFinalIntegerValue","GetFinalIntegerValue method [Windows Animation]","GetFinalIntegerValue method [Windows Animation]","IUIAnimationVariable interface","IUIAnimationVariable interface [Windows Animation]","GetFinalIntegerValue method","IUIAnimationVariable.GetFinalIntegerValue","IUIAnimationVariable::GetFinalIntegerValue","uianimation.iuianimationvariable_getfinalintegervalue","uianimation/IUIAnimationVariable::GetFinalIntegerValue"]
old-location: uianimation\iuianimationvariable_getfinalintegervalue.htm
tech.root: UIAnimation
ms.assetid: 19d71abc-e3f8-48d4-9ceb-5920dcc9c007
ms.date: 12/05/2018
ms.keywords: GetFinalIntegerValue, GetFinalIntegerValue method [Windows Animation], GetFinalIntegerValue method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetFinalIntegerValue method, IUIAnimationVariable.GetFinalIntegerValue, IUIAnimationVariable::GetFinalIntegerValue, uianimation.iuianimationvariable_getfinalintegervalue, uianimation/IUIAnimationVariable::GetFinalIntegerValue
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
 - IUIAnimationVariable::GetFinalIntegerValue
 - uianimation/IUIAnimationVariable::GetFinalIntegerValue
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
 - IUIAnimationVariable.GetFinalIntegerValue
---

# IUIAnimationVariable::GetFinalIntegerValue


## -description

Gets the final value of the animation variable as an integer.      
   This is the value after all currently scheduled animations have completed.

## -parameters

### -param finalValue [out]

The final value of the animation variable, converted to an <b>INT32</b> value.

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

To specify the rounding mode to be used when converting the value, use the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setroundingmode">IUIAnimationVariable::SetRoundingMode</a> method.

The result can also be affected by the lower and upper bounds determined by <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a> and <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>, respectively.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalvalue">IUIAnimationVariable::GetFinalValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">IUIAnimationVariable::SetLowerBound</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setroundingmode">IUIAnimationVariable::SetRoundingMode</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">IUIAnimationVariable::SetUpperBound</a>