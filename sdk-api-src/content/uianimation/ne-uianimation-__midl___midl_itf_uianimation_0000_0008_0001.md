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

# __MIDL___MIDL_itf_UIAnimation_0000_0008_0001 enumeration


## -description



         Defines potential effects on a storyboard if a priority comparison returns false.


## -enum-fields




### -field UI_ANIMATION_PRIORITY_EFFECT_FAILURE


              This storyboard might not be successfully scheduled.


### -field UI_ANIMATION_PRIORITY_EFFECT_DELAY


              The storyboard will be scheduled, but might start playing later.


## -remarks



This enumeration is used as the <i>priorityEffect</i> parameter of  <a href="https://msdn.microsoft.com/82a90bd1-7bcf-4849-bad1-bae425169a2f">IUIAnimationPriorityComparison::HasPriority</a>, informing the client of the potential effect on the storyboard to be scheduled when the return value is false (S_FALSE).  UI_ANIMATION_PRIORITY_EFFECT_FAILURE means that the  attempt to schedule the storyboard might fail if the return value is false.   UI_ANIMATION_PRIORITY_EFFECT_DELAY means that the attempt to schedule the storyboard will succeed, but if the return value is false, the storyboard could play later than it would otherwise.

  This enumeration can help an application decide how aggressive to be about reducing latency in the UI. For example, if the application returns true when the effect is UI_ANIMATION_PRIORITY_EFFECT_DELAY, then other animations might get canceled or compressed even though doing so was not strictly necessary to play a new animation within the application-specified longest acceptable delay.




## -see-also




<a href="https://msdn.microsoft.com/82a90bd1-7bcf-4849-bad1-bae425169a2f">
               IUIAnimationPriorityComparison::HasPriority</a>
 

 

