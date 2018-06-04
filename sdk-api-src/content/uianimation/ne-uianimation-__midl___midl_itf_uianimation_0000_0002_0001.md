---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

