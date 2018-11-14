---
UID: NF:uianimation.IUIAnimationVariable.GetFinalIntegerValue
title: IUIAnimationVariable::GetFinalIntegerValue
author: windows-sdk-content
description: Gets the final value of the animation variable as an integer. This is the value after all currently scheduled animations have completed.
old-location: uianimation\iuianimationvariable_getfinalintegervalue.htm
tech.root: UIAnimation
ms.assetid: 19d71abc-e3f8-48d4-9ceb-5920dcc9c007
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetFinalIntegerValue, GetFinalIntegerValue method [Windows Animation], GetFinalIntegerValue method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetFinalIntegerValue method, IUIAnimationVariable.GetFinalIntegerValue, IUIAnimationVariable::GetFinalIntegerValue, uianimation.iuianimationvariable_getfinalintegervalue, uianimation/IUIAnimationVariable::GetFinalIntegerValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationVariable.GetFinalIntegerValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationVariable.GetFinalIntegerValue
: 
---

# IUIAnimationVariable::GetFinalIntegerValue


## -description


Gets the final value of the animation variable as an integer.      
   This is the value after all currently scheduled animations have completed.


## -parameters




### -param finalValue [out]

The final value of the animation variable, converted to an <b>INT32</b> value.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.

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



To specify the rounding mode to be used when converting the value, use the <a href="https://msdn.microsoft.com/e8c86195-14a1-4535-9fc2-4992c8090e79">IUIAnimationVariable::SetRoundingMode</a> method.

The result can also be affected by the lower and upper bounds determined by <a href="https://msdn.microsoft.com/1e8f1106-6320-4670-867a-24ce6597026e">IUIAnimationVariable::SetLowerBound</a> and <a href="https://msdn.microsoft.com/d202f453-2e69-415b-823c-5a3279722274">IUIAnimationVariable::SetUpperBound</a>, respectively.




## -see-also




<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/577f83c1-aba7-4a51-82dc-68a103a31377">IUIAnimationVariable::GetFinalValue</a>



<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">IUIAnimationVariable::GetIntegerValue</a>



<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="https://msdn.microsoft.com/1e8f1106-6320-4670-867a-24ce6597026e">IUIAnimationVariable::SetLowerBound</a>



<a href="https://msdn.microsoft.com/e8c86195-14a1-4535-9fc2-4992c8090e79">IUIAnimationVariable::SetRoundingMode</a>



<a href="https://msdn.microsoft.com/d202f453-2e69-415b-823c-5a3279722274">IUIAnimationVariable::SetUpperBound</a>
 

 

