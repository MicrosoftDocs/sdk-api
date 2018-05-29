---
UID: NF:uianimation.IUIAnimationStoryboardEventHandler.OnStoryboardUpdated
title: IUIAnimationStoryboardEventHandler::OnStoryboardUpdated
author: windows-sdk-content
description: Handles events that occur when a storyboard is updated.
old-location: uianimation\iuianimationstoryboardeventhandler_onstoryboardupdated.htm
old-project: UIAnimation
ms.assetid: e1a6349e-9c3f-49e5-8e50-b51bf260e9be
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationStoryboardEventHandler interface [Windows Animation],OnStoryboardUpdated method, IUIAnimationStoryboardEventHandler.OnStoryboardUpdated, IUIAnimationStoryboardEventHandler::OnStoryboardUpdated, OnStoryboardUpdated, OnStoryboardUpdated method [Windows Animation], OnStoryboardUpdated method [Windows Animation],IUIAnimationStoryboardEventHandler interface, uianimation.iuianimationstoryboardeventhandler_onstoryboardupdated, uianimation/IUIAnimationStoryboardEventHandler::OnStoryboardUpdated
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationStoryboardEventHandler.OnStoryboardUpdated
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboardEventHandler::OnStoryboardUpdated


## -description



      Handles events that occur when a storyboard is updated.


## -parameters




### -param storyboard [in]


            The storyboard that has been updated.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method is called when the value of at least one of the variables that a storyboard is animating has changed since the last call to the <a href="https://msdn.microsoft.com/6008fe44-8d86-4a56-a1e2-7bc144b224b2">IUIAnimationManager::Update</a> method.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnStoryboardUpdated</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">IUIAnimationManager::GetStoryboardFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/611c5341-f225-461d-9718-a2432d796764">IUIAnimationManager::GetVariableFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">IUIAnimationStoryboard::GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/56042549-d6f6-4eed-8079-c1b14acbe160">IUIAnimationVariable::GetCurrentStoryboard</a>
</li>
<li>
<a href="https://msdn.microsoft.com/19d71abc-e3f8-48d4-9ceb-5920dcc9c007">IUIAnimationVariable::GetFinalIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/577f83c1-aba7-4a51-82dc-68a103a31377">IUIAnimationVariable::GetFinalValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">IUIAnimationVariable::GetIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">IUIAnimationVariable::GetPreviousIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/405bc35e-8b38-40fb-acf4-107fa6dd161a">IUIAnimationVariable::GetPreviousValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2731d302-dc52-4a10-8012-a246856d132b">IUIAnimationVariable::GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/51ae200a-a630-44fd-afd4-33d1b1dbf6d7">IUIAnimationVariable::GetValue</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6008fe44-8d86-4a56-a1e2-7bc144b224b2">IUIAnimationManager::Update</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/901afd34-03cc-4421-a467-9d096e1458fe">
      IUIAnimationStoryboard::GetElapsedTime
      </a>



<a href="https://msdn.microsoft.com/f43f53f9-1491-4847-89ef-e65ba98a2127">IUIAnimationStoryboardEventHandler</a>
 

 

