---
UID: NF:uianimation.IUIAnimationVariable.GetPreviousValue
title: IUIAnimationVariable::GetPreviousValue
author: windows-sdk-content
description: Gets the previous value of the animation variable. This is the value of the animation variable before the most recent update.
old-location: uianimation\iuianimationvariable_getpreviousvalue.htm
tech.root: UIAnimation
ms.assetid: 405bc35e-8b38-40fb-acf4-107fa6dd161a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPreviousValue, GetPreviousValue method [Windows Animation], GetPreviousValue method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetPreviousValue method, IUIAnimationVariable.GetPreviousValue, IUIAnimationVariable::GetPreviousValue, uianimation.iuianimationvariable_getpreviousvalue, uianimation/IUIAnimationVariable::GetPreviousValue
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
 - IUIAnimationVariable.GetPreviousValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationVariable::GetPreviousValue


## -description


Gets the previous value of the animation variable. This is the value of the animation variable before the most recent update.


## -parameters




### -param previousValue [out]

The previous value of the animation variable.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The results can be affected by the lower and upper bounds determined by <a href="https://msdn.microsoft.com/1e8f1106-6320-4670-867a-24ce6597026e">IUIAnimationVariable::SetLowerBound</a> and <a href="https://msdn.microsoft.com/d202f453-2e69-415b-823c-5a3279722274">IUIAnimationVariable::SetUpperBound</a>, respectively.




## -see-also




<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/577f83c1-aba7-4a51-82dc-68a103a31377">IUIAnimationVariable::GetFinalValue</a>



<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="https://msdn.microsoft.com/1e8f1106-6320-4670-867a-24ce6597026e">IUIAnimationVariable::SetLowerBound</a>



<a href="https://msdn.microsoft.com/d202f453-2e69-415b-823c-5a3279722274">IUIAnimationVariable::SetUpperBound</a>
 

 

