---
UID: NF:uianimation.IUIAnimationVariableChangeHandler.OnValueChanged
title: IUIAnimationVariableChangeHandler::OnValueChanged
author: windows-sdk-content
description: Handles events that occur when the value of an animation variable changes.
old-location: uianimation\iuianimationvariablechangehandler_onvaluechanged.htm
old-project: UIAnimation
ms.assetid: 1e865f55-d703-4d91-8690-b816b5fe1a89
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationVariableChangeHandler interface [Windows Animation],OnValueChanged method, IUIAnimationVariableChangeHandler.OnValueChanged, IUIAnimationVariableChangeHandler::OnValueChanged, OnValueChanged, OnValueChanged method [Windows Animation], OnValueChanged method [Windows Animation],IUIAnimationVariableChangeHandler interface, uianimation.iuianimationvariablechangehandler_onvaluechanged, uianimation/IUIAnimationVariableChangeHandler::OnValueChanged
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
 - IUIAnimationVariableChangeHandler.OnValueChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariableChangeHandler::OnValueChanged


## -description



      Handles events that occur when the value of an animation variable changes.

This method receives updates as <b>DOUBLE</b> values.  
         To receive updates as <b>INT32</b> values, use the <a href="https://msdn.microsoft.com/e12224a2-c8f3-45eb-a254-d624de16e12d">
         IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged</a> method.


## -parameters




### -param storyboard [in]


            The storyboard that is animating the animation variable specified by the <i>variable</i> parameter.


### -param variable [in]


            The animation variable that has been updated.


### -param newValue [in]


            The new value of the animation variable.


### -param previousValue [in]


            The previous value of the animation variable.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnValueChanged</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/51ae200a-a630-44fd-afd4-33d1b1dbf6d7">IUIAnimationVariable::GetValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/577f83c1-aba7-4a51-82dc-68a103a31377">IUIAnimationVariable::GetFinalValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/405bc35e-8b38-40fb-acf4-107fa6dd161a">IUIAnimationVariable::GetPreviousValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">IUIAnimationVariable::GetIntegerValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/19d71abc-e3f8-48d4-9ceb-5920dcc9c007">IUIAnimationVariable::GetFinalIntegerValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">IUIAnimationVariable::GetPreviousIntegerValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/56042549-d6f6-4eed-8079-c1b14acbe160">IUIAnimationVariable::GetCurrentStoryboard
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/611c5341-f225-461d-9718-a2432d796764">IUIAnimationManager::GetVariableFromTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">IUIAnimationManager::GetStoryboardFromTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">IUIAnimationStoryboard::GetTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2731d302-dc52-4a10-8012-a246856d132b">IUIAnimationVariable::GetTag
</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/405bc35e-8b38-40fb-acf4-107fa6dd161a">
      IUIAnimationVariable::GetPreviousValue</a>



<a href="https://msdn.microsoft.com/51ae200a-a630-44fd-afd4-33d1b1dbf6d7">
      IUIAnimationVariable::GetValue</a>



<a href="https://msdn.microsoft.com/d773a59f-10a5-41e4-92f1-af72d8d15105">IUIAnimationVariable::SetVariableChangeHandler</a>



<a href="https://msdn.microsoft.com/2288b256-aaf4-44fe-9ad1-f05ef7b0e30b">IUIAnimationVariableChangeHandler</a>



<a href="https://msdn.microsoft.com/e12224a2-c8f3-45eb-a254-d624de16e12d">
         IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged</a>
 

 

