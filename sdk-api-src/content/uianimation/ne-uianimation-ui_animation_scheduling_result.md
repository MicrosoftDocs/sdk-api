---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0002_0002
title: UI_ANIMATION_SCHEDULING_RESULT (uianimation.h)
author: windows-sdk-content
description: Defines results for storyboard scheduling.
old-location: uianimation\ui_animation_scheduling_result.htm
tech.root: UIAnimation
ms.assetid: 2d62589a-9121-4af6-b704-566a28dcc21e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED, UI_ANIMATION_SCHEDULING_DEFERRED, UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY, UI_ANIMATION_SCHEDULING_RESULT, UI_ANIMATION_SCHEDULING_RESULT enumeration [Windows Animation], UI_ANIMATION_SCHEDULING_SUCCEEDED, UI_ANIMATION_SCHEDULING_UNEXPECTED_FAILURE, uianimation.ui_animation_scheduling_result, uianimation/UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED, uianimation/UI_ANIMATION_SCHEDULING_DEFERRED, uianimation/UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY, uianimation/UI_ANIMATION_SCHEDULING_RESULT, uianimation/UI_ANIMATION_SCHEDULING_SUCCEEDED, uianimation/UI_ANIMATION_SCHEDULING_UNEXPECTED_FAILURE
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAnimation.h
api_name:
 - UI_ANIMATION_SCHEDULING_RESULT
product: Windows
targetos: Windows
req.typenames: UI_ANIMATION_SCHEDULING_RESULT
req.redist: 
---

# UI_ANIMATION_SCHEDULING_RESULT enumeration


## -description


Defines results for storyboard scheduling.


## -enum-fields




### -field UI_ANIMATION_SCHEDULING_UNEXPECTED_FAILURE

Scheduling failed for an unexpected reason.


### -field UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY

Scheduling failed because
               a scheduling conflict occurred and the currently scheduled storyboard has higher priority.
               
               For more information, see <a href="https://msdn.microsoft.com/82a90bd1-7bcf-4849-bad1-bae425169a2f">IUIAnimationPriorityComparison::HasPriority</a>.


### -field UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED

Scheduling failed because 
               the storyboard is already scheduled.


### -field UI_ANIMATION_SCHEDULING_SUCCEEDED

Scheduling succeeded.


### -field UI_ANIMATION_SCHEDULING_DEFERRED

Scheduling is deferred and will be attempted when the current callback completes.


## -remarks




<a href="https://msdn.microsoft.com/b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8">IUIAnimationStoryboard::Schedule</a> returns UI_ANIMATION_SCHEDULING_DEFERRED only if the application attempts to schedule a storyboard during a callback to <a href="https://msdn.microsoft.com/e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd">IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged</a>.




## -see-also




<a href="https://msdn.microsoft.com/b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8">IUIAnimationStoryboard::Schedule</a>
 

 

