---
UID: NF:uianimation.IUIAnimationStoryboard2.Schedule
title: IUIAnimationStoryboard2::Schedule
author: windows-sdk-content
description: Directs the storyboard to schedule itself for play.
old-location: uianimation\iuianimationstoryboard2_schedule.htm
tech.root: UIAnimation
ms.assetid: 9F20AE4A-F693-4DDA-90F4-FCCA5291208B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAnimationStoryboard2 interface [Windows Animation],Schedule method, IUIAnimationStoryboard2.Schedule, IUIAnimationStoryboard2::Schedule, Schedule, Schedule method [Windows Animation], Schedule method [Windows Animation],IUIAnimationStoryboard2 interface, uianimation.iuianimationstoryboard2_schedule, uianimation/IUIAnimationStoryboard2::Schedule
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
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
 - IUIAnimationStoryboard2.Schedule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard2::Schedule


## -description


Directs the storyboard to schedule itself for play.


## -parameters




### -param timeNow [in]

The current time.


### -param schedulingResult [out, optional]

The result of the scheduling request.
            You can omit this parameter from calls to this method.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method directs a storyboard to try to add itself to the schedule of playing storyboards, using these rules:

<ul>
<li>
If there are no playing storyboards animating any of the same animation variables, the attempt succeeds and the storyboard starts playing immediately.

</li>
<li>
If the storyboard has priority to cancel, trim, conclude, or compress conflicting storyboards, the attempt to schedule succeeds and the storyboard starts playing as soon as possible.

</li>
<li>
If the storyboard does not have priority, the attempt fails and the <i>schedulingResult</i> parameter is set to <a href="https://msdn.microsoft.com/en-us/library/Dd371967(v=VS.85).aspx">UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY</a>.

</li>
</ul>
If this method is called from a handler for <a href="https://msdn.microsoft.com/e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd">OnStoryboardStatusChanged</a> events, the <i>schedulingResult</i> parameter is set to <b>UI_ANIMATION_SCHEDULING_DEFERRED</b>.  The only way to determine whether the storyboard is successfully scheduled is to set a storyboard event handler and check whether the storyboard's status ever becomes <a href="https://msdn.microsoft.com/en-us/library/Dd371967(v=VS.85).aspx">UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY</a>.

It is possible to reuse a storyboard by calling <b>Schedule</b> again after its status has reached <a href="https://msdn.microsoft.com/en-us/library/Dd371971(v=VS.85).aspx">UI_ANIMATION_STORYBOARD_READY</a>.  An attempt to schedule a storyboard when it is in any state other than <b>UI_ANIMATION_STORYBOARD_BUILDING</b> or <b>UI_ANIMATION_STORYBOARD_READY</b> fails, and  <i>schedulingResult</i> is set to <a href="https://msdn.microsoft.com/en-us/library/Dd371967(v=VS.85).aspx">UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED</a>.




## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/ABB7184F-A703-45E3-96D8-E3062EEB9565">IUIAnimationStoryboard2::Abandon</a>



<a href="https://msdn.microsoft.com/C7687E52-433F-4E73-910D-86298E528F7B">IUIAnimationStoryboard2::Conclude</a>



<a href="https://msdn.microsoft.com/632BC77D-F2C5-4D08-8E9C-0598617A1DA7">IUIAnimationStoryboard2::Finish</a>



<a href="https://msdn.microsoft.com/1694B720-891A-4214-A009-6AA722E5B83D">IUIAnimationStoryboard2::GetStatus</a>



<a href="https://msdn.microsoft.com/32654e4b-158b-4d1a-afc7-98f90212b33b">IUIAnimationTimer::GetTime</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371967(v=VS.85).aspx">UI_ANIMATION_SCHEDULING_RESULT</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371971(v=VS.85).aspx">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

