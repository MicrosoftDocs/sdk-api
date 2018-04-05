---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0002_0001
title: "__MIDL___MIDL_itf_UIAnimation_0000_0002_0001"
author: windows-driver-content
description: Defines the status for a storyboard.
old-location: uianimation\ui_animation_storyboard_status.htm
old-project: UIAnimation
ms.assetid: 02830092-0070-44dc-8db2-239941134473
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: UI_ANIMATION_STORYBOARD_BUILDING, UI_ANIMATION_STORYBOARD_CANCELLED, UI_ANIMATION_STORYBOARD_FINISHED, UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY, UI_ANIMATION_STORYBOARD_PLAYING, UI_ANIMATION_STORYBOARD_READY, UI_ANIMATION_STORYBOARD_SCHEDULED, UI_ANIMATION_STORYBOARD_STATUS, UI_ANIMATION_STORYBOARD_STATUS enumeration [Windows Animation], UI_ANIMATION_STORYBOARD_TRUNCATED, __MIDL___MIDL_itf_UIAnimation_0000_0002_0001, uianimation.ui_animation_storyboard_status, uianimation/UI_ANIMATION_STORYBOARD_BUILDING, uianimation/UI_ANIMATION_STORYBOARD_CANCELLED, uianimation/UI_ANIMATION_STORYBOARD_FINISHED, uianimation/UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY, uianimation/UI_ANIMATION_STORYBOARD_PLAYING, uianimation/UI_ANIMATION_STORYBOARD_READY, uianimation/UI_ANIMATION_STORYBOARD_SCHEDULED, uianimation/UI_ANIMATION_STORYBOARD_STATUS, uianimation/UI_ANIMATION_STORYBOARD_TRUNCATED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: UI_ANIMATION_STORYBOARD_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	UIAnimation.h
api_name:
-	UI_ANIMATION_STORYBOARD_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL___MIDL_itf_UIAnimation_0000_0002_0001 enumeration


## -description



         Defines  the status for a storyboard.


## -enum-fields




### -field UI_ANIMATION_STORYBOARD_BUILDING


               The storyboard has never been scheduled.


### -field UI_ANIMATION_STORYBOARD_SCHEDULED


               The storyboard is scheduled to play.


### -field UI_ANIMATION_STORYBOARD_CANCELLED


               The storyboard was canceled.


### -field UI_ANIMATION_STORYBOARD_PLAYING


               The storyboard is currently playing.


### -field UI_ANIMATION_STORYBOARD_TRUNCATED


               The storyboard was truncated.


### -field UI_ANIMATION_STORYBOARD_FINISHED


               The storyboard has finished playing.


### -field UI_ANIMATION_STORYBOARD_READY


               The storyboard is built and ready for scheduling.


### -field UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY


               Scheduling the storyboard failed because a scheduling conflict occurred and the currently scheduled storyboard has higher priority.


## -remarks



Unless <a href="https://msdn.microsoft.com/8ee9a17f-c57c-49df-950d-491e05ba8768">IUIAnimationStoryboard::GetStatus</a> is called from a handler for <a href="https://msdn.microsoft.com/e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd">OnStoryboardStatusChanged</a> events, it returns only the following status values:

<ul>
<li>UI_ANIMATION_STORYBOARD_BUILDING</li>
<li>UI_ANIMATION_STORYBOARD_SCHEDULED</li>
<li>UI_ANIMATION_STORYBOARD_PLAYING</li>
<li>UI_ANIMATION_STORYBOARD_READY</li>
</ul>
All status values can be passed to  <a href="https://msdn.microsoft.com/e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd">IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged</a>.

The following diagram illustrates the transitions between these states.

<img alt="Diagram that shows how the animation manager schedules the storyboard and manages the animation." src="images/StateDiagram.png"/>




## -see-also




<a href="https://msdn.microsoft.com/8ee9a17f-c57c-49df-950d-491e05ba8768">
               IUIAnimationStoryboard::GetStatus</a>



<a href="https://msdn.microsoft.com/e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd">
               IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged</a>
 

 

