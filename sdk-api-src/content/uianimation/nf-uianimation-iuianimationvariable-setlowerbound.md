---
UID: NF:uianimation.IUIAnimationVariable.SetLowerBound
title: IUIAnimationVariable::SetLowerBound (uianimation.h)
author: windows-sdk-content
description: Sets the lower bound (floor) for the animation variable. The value of the animation variable should not fall below the specified value.
old-location: uianimation\iuianimationvariable_setlowerbound.htm
tech.root: UIAnimation
ms.assetid: 1e8f1106-6320-4670-867a-24ce6597026e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetLowerBound method, IUIAnimationVariable.SetLowerBound, IUIAnimationVariable::SetLowerBound, SetLowerBound, SetLowerBound method [Windows Animation], SetLowerBound method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_setlowerbound, uianimation/IUIAnimationVariable::SetLowerBound
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
 - IUIAnimationVariable.SetLowerBound
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationVariable::SetLowerBound


## -description


Sets the lower bound (floor) for the animation variable. The value of the animation variable should not fall below the specified value.


## -parameters




### -param bound [in]

The lower bound for the animation variable.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/19d71abc-e3f8-48d4-9ceb-5920dcc9c007">IUIAnimationVariable::GetFinalIntegerValue</a>



<a href="https://msdn.microsoft.com/577f83c1-aba7-4a51-82dc-68a103a31377">IUIAnimationVariable::GetFinalValue</a>



<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">IUIAnimationVariable::GetIntegerValue</a>



<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="https://msdn.microsoft.com/405bc35e-8b38-40fb-acf4-107fa6dd161a">IUIAnimationVariable::GetPreviousValue</a>



<a href="https://msdn.microsoft.com/51ae200a-a630-44fd-afd4-33d1b1dbf6d7">IUIAnimationVariable::GetValue</a>



<a href="https://msdn.microsoft.com/d202f453-2e69-415b-823c-5a3279722274">IUIAnimationVariable::SetUpperBound</a>
 

 

