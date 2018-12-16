---
UID: NN:uianimation.IUIAnimationTransition
title: IUIAnimationTransition
author: windows-sdk-content
description: Defines a transition, which determines how an animation variable changes over time.
old-location: uianimation\iuianimationtransition.htm
tech.root: UIAnimation
ms.assetid: 99804a2f-82c9-494c-b75d-69e66f1e49ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAnimationTransition, IUIAnimationTransition interface [Windows Animation], IUIAnimationTransition interface [Windows Animation],described, uianimation.iuianimationtransition, uianimation/IUIAnimationTransition
ms.topic: interface
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
 - IUIAnimationTransition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationTransition interface


## -description


Defines a transition, which determines how an animation variable changes over time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTransition</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTransition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTransition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc46ca31-3146-4d93-b859-79fe5e1fea08">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cb22573-a318-4682-bc82-0a81c9dbdcbe">IsDurationKnown</a>
</td>
<td align="left" width="63%">
Determines whether the transition's duration is currently known.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e931eee-8b28-4be2-a760-8f62b5ce89ed">SetInitialValue</a>
</td>
<td align="left" width="63%">
Sets the initial value for the transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adb5a173-6efa-4b1b-8e2f-1d69288653ae">SetInitialVelocity</a>
</td>
<td align="left" width="63%">
Sets the initial velocity for the transition.

</td>
</tr>
</table> 


## -remarks



<b>IUIAnimationTransition</b> is one of the primary interfaces used to add animation to an application,
         along with 
         the <a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a> and 
         <a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a> interfaces.


<a href="https://msdn.microsoft.com/041b054b-609f-40ed-a348-bd44e965a00e">UIAnimationTransitionLibrary</a> implements
         a library of standard transitions.




## -see-also




<a href="https://msdn.microsoft.com/0178b674-2ad3-49ee-92ce-925840ab8409">IUIAnimationManager::ScheduleTransition</a>



<a href="https://msdn.microsoft.com/c3213e5d-c8f5-406a-bc44-9de7a740b070">IUIAnimationStoryboard::AddTransition</a>



<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">IUIAnimationStoryboard::AddTransitionAtKeyframes</a>



<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/62aec8da-e067-4b61-9465-e07fb5b42b7f">IUIAnimationTransitionFactory</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/d37718ac-0256-4a24-a26c-d29173593be0">Storyboard Overview</a>
 

 

