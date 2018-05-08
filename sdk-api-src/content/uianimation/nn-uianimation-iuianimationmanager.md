---
UID: NN:uianimation.IUIAnimationManager
title: IUIAnimationManager
author: windows-driver-content
description: Defines the animation manager, which provides a central interface for creating and managing animations.
old-location: uianimation\iuianimationmanager.htm
old-project: UIAnimation
ms.assetid: 21f16c65-90aa-4b1f-93bc-8ee0488c6ded
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IUIAnimationManager, IUIAnimationManager interface [Windows Animation], IUIAnimationManager interface [Windows Animation],described, uianimation.iuianimationmanager, uianimation/IUIAnimationManager
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationManager
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager interface


## -description



      Defines the animation manager, which provides a central interface for creating and managing animations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cecb0026-ed6f-48b8-9381-d020a36e7e87">
         AbandonAllStoryboards</a>
</td>
<td align="left" width="63%">
Abandons all active storyboards.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4c38e78-1b9e-4918-ba15-6a4c5c390c07">
         CreateAnimationVariable</a>
</td>
<td align="left" width="63%">

         Creates a new animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/933ffb62-0f69-4225-873b-e2e023939bea">
         CreateStoryboard</a>
</td>
<td align="left" width="63%">

         Creates a new storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db5ba70c-3904-4053-881a-b1412beb35f3">
         FinishAllStoryboards</a>
</td>
<td align="left" width="63%">

         Finishes all active storyboards within the specified time interval.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/838140c3-12ca-4909-a0f8-713b5472e5a9">
         GetStatus</a>
</td>
<td align="left" width="63%">

         Gets the status of the animation manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">
         GetStoryboardFromTag</a>
</td>
<td align="left" width="63%">

         Gets the storyboard with the specified tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/611c5341-f225-461d-9718-a2432d796764">
         GetVariableFromTag</a>
</td>
<td align="left" width="63%">

         Gets the animation variable with the specified tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52b11e79-9930-4fd8-84b4-152917090519">
         Pause</a>
</td>
<td align="left" width="63%">

         Pauses all animations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f29a9337-0ed0-46f8-ab77-8f82ab39d8df">
         Resume</a>
</td>
<td align="left" width="63%">

         Resumes all animations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0178b674-2ad3-49ee-92ce-925840ab8409">
         ScheduleTransition</a>
</td>
<td align="left" width="63%">

         Creates and schedules a single-transition storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5d6c5f1-1e1c-497f-a556-f419e2c68585">
         SetAnimationMode</a>
</td>
<td align="left" width="63%">

         Sets the animation mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cea146d1-4a9c-4089-8015-ac16602f5afd">
         SetCancelPriorityComparison</a>
</td>
<td align="left" width="63%">

         Sets a priority comparison handler for cancelation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf2a7782-3541-483e-8d5e-3e82693f103c">
         SetCompressPriorityComparison</a>
</td>
<td align="left" width="63%">

         Sets a priority comparison handler for compression.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00a3d7e4-7ad2-46a8-a9c2-0e725005c00b">
         SetConcludePriorityComparison</a>
</td>
<td align="left" width="63%">

         Sets a priority comparison handler for conclusion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27182009-1614-41a0-9b55-7c1dcb494883">
         SetDefaultLongestAcceptableDelay</a>
</td>
<td align="left" width="63%">

         Sets the default acceptable animation delay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89c4df40-6faa-4b7c-a255-289d1f8a6254">
         SetManagerEventHandler</a>
</td>
<td align="left" width="63%">

         Specifies a handler for animation manager status updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4c81cc4-4c00-4f78-819d-55f79972fe46">
         SetTrimPriorityComparison</a>
</td>
<td align="left" width="63%">

         Sets a priority comparison handler for trimming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bcce52c-d29a-423c-ae76-eb88cbe8c8df">
         Shutdown</a>
</td>
<td align="left" width="63%">

         Shuts down the animation manager and all its associated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6008fe44-8d86-4a56-a1e2-7bc144b224b2">
         Update</a>
</td>
<td align="left" width="63%">
Updates the values of all animation variables.

</td>
</tr>
</table> 


## -remarks



<b>IUIAnimationManager</b> defines a central control object for animations.
         
         A single instance of <b>IUIAnimationManager</b> is typically used to compose, schedule, 
         and manage all animations for a client application.


<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>,
         <a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>, and 
         <a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>
         are the primary components for building animations.
         
         Use <b>IUIAnimationManager</b> to create and manage these components.


#### Examples

For an example that creates the animation manager object, see <a href="https://msdn.microsoft.com/4005819e-482c-4052-89f8-b8e457c0c3dc">Create the Main Animation Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

