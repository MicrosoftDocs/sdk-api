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

# __MIDL___MIDL_itf_UIAnimation_0000_0002_0002 enumeration


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




<a href="https://msdn.microsoft.com/b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8">
               IUIAnimationStoryboard::Schedule</a>
 

 

