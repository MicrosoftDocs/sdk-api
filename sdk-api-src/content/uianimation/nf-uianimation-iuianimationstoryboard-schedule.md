---
UID: NF:uianimation.IUIAnimationStoryboard.Schedule
title: IUIAnimationStoryboard::Schedule (uianimation.h)
description: Directs the storyboard to schedule itself for play. (IUIAnimationStoryboard.Schedule)
helpviewer_keywords: ["IUIAnimationStoryboard interface [Windows Animation]","Schedule method","IUIAnimationStoryboard.Schedule","IUIAnimationStoryboard::Schedule","Schedule","Schedule method [Windows Animation]","Schedule method [Windows Animation]","IUIAnimationStoryboard interface","uianimation.iuianimationstoryboard_schedule","uianimation/IUIAnimationStoryboard::Schedule"]
old-location: uianimation\iuianimationstoryboard_schedule.htm
tech.root: UIAnimation
ms.assetid: b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],Schedule method, IUIAnimationStoryboard.Schedule, IUIAnimationStoryboard::Schedule, Schedule, Schedule method [Windows Animation], Schedule method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_schedule, uianimation/IUIAnimationStoryboard::Schedule
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationStoryboard::Schedule
 - uianimation/IUIAnimationStoryboard::Schedule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationStoryboard.Schedule
---

# IUIAnimationStoryboard::Schedule


## -description

Directs the storyboard to schedule itself for play.

## -parameters

### -param timeNow [in]

The current time.

### -param schedulingResult [out, optional]

The result of the scheduling request.
            This parameter can be omitted from calls to this method.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method directs a storyboard to attempt to add itself to the schedule of playing storyboards. The rules are as follows:

<ul>
<li>
If there are no playing storyboards animating any of the same animation variables, the attempt succeeds and the storyboard starts playing immediately.

</li>
<li>
If the storyboard has priority to cancel, trim, conclude, or compress conflicting storyboards, the attempt to schedule succeeds and the storyboard begins playing as soon as possible.

</li>
<li>
If the storyboard does not have priority, the attempt fails and the <i>schedulingResult</i> parameter is set to <b>UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY</b>.

</li>
</ul>
If this method is called from a handler for <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">OnStoryboardStatusChanged</a> events, the <i>schedulingResult</i> parameter is set to <b>UI_ANIMATION_SCHEDULING_DEFERRED</b>.  The only way to determine whether the storyboard is successfully scheduled is to set a storyboard event handler and check whether the storyboard's status ever becomes <b>UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY</b>.

It is possible reuse a storyboard by calling <b>Schedule</b> again after its status has reached <b>UI_ANIMATION_STORYBOARD_READY</b>.  An attempt to schedule a storyboard when it is in any state other than <b>UI_ANIMATION_STORYBOARD_BUILDING</b> or <b>UI_ANIMATION_STORYBOARD_READY</b> fails, and  <i>schedulingResult</i> is set to <b>UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED</b>.


#### Examples

The following example gets the current time and schedules the storyboard. For an additional example, see <a href="/windows/desktop/UIAnimation/scheduling-a-storyboard">Schedule a Storyboard</a>.


```cpp
// Get the current time and schedule the storyboard
UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    UI_ANIMATION_SCHEDULING_RESULT schedulingResult;
    hr = pStoryboard->Schedule(
        secondsNow,
        &schedulingResult
        );
    if (SUCCEEDED(hr))
    {
        if (schedulingResult == UI_ANIMATION_SCHEDULING_SUCCEEDED)
        {
            ...
        }
        else
        {
            ...
        }
    }
}
```

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-abandon">IUIAnimationStoryboard::Abandon</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-conclude">IUIAnimationStoryboard::Conclude</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-finish">IUIAnimationStoryboard::Finish</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-gettime">IUIAnimationTimer::GetTime</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_scheduling_result">UI_ANIMATION_SCHEDULING_RESULT</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
