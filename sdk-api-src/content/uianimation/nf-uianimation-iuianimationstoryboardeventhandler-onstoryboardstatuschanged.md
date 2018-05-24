---
UID: NF:uianimation.IUIAnimationStoryboardEventHandler.OnStoryboardStatusChanged
title: IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged
author: windows-driver-content
description: Handles events that occur when a storyboard's status changes.
old-location: uianimation\iuianimationstoryboardeventhandler_onstoryboardstatuschanged.htm
old-project: UIAnimation
ms.assetid: e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IUIAnimationStoryboardEventHandler interface [Windows Animation],OnStoryboardStatusChanged method, IUIAnimationStoryboardEventHandler.OnStoryboardStatusChanged, IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged, OnStoryboardStatusChanged, OnStoryboardStatusChanged method [Windows Animation], OnStoryboardStatusChanged method [Windows Animation],IUIAnimationStoryboardEventHandler interface, uianimation.iuianimationstoryboardeventhandler_onstoryboardstatuschanged, uianimation/IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IUIAnimationStoryboardEventHandler.OnStoryboardStatusChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged


## -description



      Handles events that occur when a storyboard's status changes.


## -parameters




### -param storyboard [in]


            The storyboard whose status has changed.


### -param newStatus [in]


            The new status.


### -param previousStatus [in]


            The previous status.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnStoryboardStatusChanged</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/e4c38e78-1b9e-4918-ba15-6a4c5c390c07">IUIAnimationManager::CreateAnimationVariable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/933ffb62-0f69-4225-873b-e2e023939bea">IUIAnimationManager::CreateStoryboard</a>
</li>
<li>
<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">IUIAnimationManager::GetStoryboardFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/611c5341-f225-461d-9718-a2432d796764">IUIAnimationManager::GetVariableFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2350dbd0-3a67-4832-94dd-56adce80a387">IUIAnimationStoryboard::Abandon</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f598c8a4-4325-49ed-bc18-5d672e089592">IUIAnimationStoryboard::AddKeyframeAtOffset</a>
</li>
<li>
<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c3213e5d-c8f5-406a-bc44-9de7a740b070">IUIAnimationStoryboard::AddTransition</a>
</li>
<li>
<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>
</li>
<li>
<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/82f915df-c031-41e9-8347-044b37793182">IUIAnimationStoryboard::Conclude</a>
</li>
<li>
<a href="https://msdn.microsoft.com/45d0872a-dbcf-4151-a880-80b2c6fb884c">IUIAnimationStoryboard::Finish</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">IUIAnimationStoryboard::GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ac5ee9c0-cecb-41f1-b8d3-6f779dfafef7">IUIAnimationStoryboard::HoldVariable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3c1ddb8c-fcbf-4b0c-8725-35dfc15e3c02">IUIAnimationStoryboard::RepeatBetweenKeyframes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5f87a4b1-8db9-42ba-963f-664db588c520">IUIAnimationStoryboard::SetLongestAcceptableDelay</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8fbe8e94-8585-4adc-8643-3962aff6a031">IUIAnimationStoryboard::SetStoryboardEventHandler</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ade41b03-9194-4b1a-a672-32bb48a2f5ba">IUIAnimationStoryboard::SetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8">IUIAnimationStoryboard::Schedule</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cc46ca31-3146-4d93-b859-79fe5e1fea08">IUIAnimationTransition::GetDuration</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5cb22573-a318-4682-bc82-0a81c9dbdcbe">IUIAnimationTransition::IsDurationKnown</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5e931eee-8b28-4be2-a760-8f62b5ce89ed">IUIAnimationTransition::SetInitialValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/adb5a173-6efa-4b1b-8e2f-1d69288653ae">IUIAnimationTransition::SetInitialVelocity</a>
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
<li>
<a href="https://msdn.microsoft.com/176b0047-cac8-474b-9126-fdab4bc41537">IUIAnimationVariable::SetTag</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/8ee9a17f-c57c-49df-950d-491e05ba8768">IUIAnimationStoryboard::GetStatus</a>



<a href="https://msdn.microsoft.com/f43f53f9-1491-4847-89ef-e65ba98a2127">IUIAnimationStoryboardEventHandler</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

