---
UID: NN:uianimation.IUIAnimationStoryboard
title: IUIAnimationStoryboard
author: windows-sdk-content
description: Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.
old-location: uianimation\iuianimationstoryboard.htm
old-project: UIAnimation
ms.assetid: 6b30b660-dfa4-410f-a8de-58ea5c9a104d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationStoryboard, IUIAnimationStoryboard interface [Windows Animation], IUIAnimationStoryboard interface [Windows Animation],described, uianimation.iuianimationstoryboard, uianimation/IUIAnimationStoryboard
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationStoryboard
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard interface


## -description



      Defines a storyboard, which contains a group of transitions
      that are synchronized relative to one another.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationStoryboard</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationStoryboard</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationStoryboard</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2350dbd0-3a67-4832-94dd-56adce80a387">
         Abandon</a>
</td>
<td align="left" width="63%">

         Directs the storyboard to abandon playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">
         AddKeyframeAfterTransition</a>
</td>
<td align="left" width="63%">

         Adds a keyfame at the end of the specified transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f598c8a4-4325-49ed-bc18-5d672e089592">
         AddKeyframeAtOffset</a>
</td>
<td align="left" width="63%">

         Adds a keyfame at the specified offset from an existing keyframe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3213e5d-c8f5-406a-bc44-9de7a740b070">
         AddTransition</a>
</td>
<td align="left" width="63%">

         Adds a transition to the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">
         AddTransitionAtKeyframe</a>
</td>
<td align="left" width="63%">

         Adds a transition that starts at the specified keyframe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">
         AddTransitionBetweenKeyframes</a>
</td>
<td align="left" width="63%">

         Adds a transition between two keyframes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82f915df-c031-41e9-8347-044b37793182">
         Conclude</a>
</td>
<td align="left" width="63%">

         Directs the storyboard to conclude.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45d0872a-dbcf-4151-a880-80b2c6fb884c">
         Finish</a>
</td>
<td align="left" width="63%">

				Directs the storyboard to finish playing within the specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/901afd34-03cc-4421-a467-9d096e1458fe">
         GetElapsedTime</a>
</td>
<td align="left" width="63%">

         Gets the time elapsed since the storyboard started playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ee9a17f-c57c-49df-950d-491e05ba8768">
         GetStatus</a>
</td>
<td align="left" width="63%">

         Gets the status of the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">
         GetTag</a>
</td>
<td align="left" width="63%">

         Gets the tag for the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac5ee9c0-cecb-41f1-b8d3-6f779dfafef7">
         HoldVariable</a>
</td>
<td align="left" width="63%">

         Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c1ddb8c-fcbf-4b0c-8725-35dfc15e3c02">
         RepeatBetweenKeyframes</a>
</td>
<td align="left" width="63%">

         Creates a loop between two specified keyframes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8">
         Schedule</a>
</td>
<td align="left" width="63%">

         Directs the storyboard to schedule itself for play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f87a4b1-8db9-42ba-963f-664db588c520">
         SetLongestAcceptableDelay</a>
</td>
<td align="left" width="63%">

         Sets the longest acceptable delay before the scheduled storyboard begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fbe8e94-8585-4adc-8643-3962aff6a031">
         SetStoryboardEventHandler</a>
</td>
<td align="left" width="63%">

         Specifies a handler for storyboard events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ade41b03-9194-4b1a-a672-32bb48a2f5ba">
         SetTag</a>
</td>
<td align="left" width="63%">

 	      Sets the tag for the storyboard.

</td>
</tr>
</table> 


## -remarks



<b>IUIAnimationStoryboard</b> is a primary component for building animations,
         along with 
         <a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a> and 
         <a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>.
         
         




## -see-also




<a href="https://msdn.microsoft.com/cecb0026-ed6f-48b8-9381-d020a36e7e87">IUIAnimationManager::AbandonAllStoryboards</a>



<a href="https://msdn.microsoft.com/933ffb62-0f69-4225-873b-e2e023939bea">IUIAnimationManager::CreateStoryboard</a>



<a href="https://msdn.microsoft.com/db5ba70c-3904-4053-881a-b1412beb35f3">IUIAnimationManager::FinishAllStoryboards</a>



<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">IUIAnimationManager::GetStoryboardFromTag</a>



<a href="https://msdn.microsoft.com/56042549-d6f6-4eed-8079-c1b14acbe160">IUIAnimationVariable::GetCurrentStoryboard</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/d37718ac-0256-4a24-a26c-d29173593be0">Storyboard Overview</a>
 

 

