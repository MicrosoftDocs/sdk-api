---
UID: NF:uianimation.IUIAnimationVariable.GetValue
title: IUIAnimationVariable::GetValue
author: windows-sdk-content
description: Gets the current value of the animation variable.
old-location: uianimation\iuianimationvariable_getvalue.htm
old-project: UIAnimation
ms.assetid: 51ae200a-a630-44fd-afd4-33d1b1dbf6d7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetValue, GetValue method [Windows Animation], GetValue method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetValue method, IUIAnimationVariable.GetValue, IUIAnimationVariable::GetValue, uianimation.iuianimationvariable_getvalue, uianimation/IUIAnimationVariable::GetValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationVariable.GetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable::GetValue


## -description



      Gets the current value of the animation variable.


## -parameters




### -param value [out]


            The current value of the animation variable.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The results can be affected by the lower and upper bounds determined by <a href="https://msdn.microsoft.com/1e8f1106-6320-4670-867a-24ce6597026e">IUIAnimationVariable::SetLowerBound</a> and <a href="https://msdn.microsoft.com/d202f453-2e69-415b-823c-5a3279722274">IUIAnimationVariable::SetUpperBound</a>, respectively.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/7abf084a-31f5-4e32-bfd1-e88fbc2bf63d">Read the Animation Variable Values</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/577f83c1-aba7-4a51-82dc-68a103a31377">
      IUIAnimationVariable::GetFinalValue</a>



<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">IUIAnimationVariable::GetIntegerValue</a>



<a href="https://msdn.microsoft.com/405bc35e-8b38-40fb-acf4-107fa6dd161a">
      IUIAnimationVariable::GetPreviousValue</a>



<a href="https://msdn.microsoft.com/1e8f1106-6320-4670-867a-24ce6597026e">IUIAnimationVariable::SetLowerBound</a>



<a href="https://msdn.microsoft.com/d202f453-2e69-415b-823c-5a3279722274">IUIAnimationVariable::SetUpperBound</a>
 

 

