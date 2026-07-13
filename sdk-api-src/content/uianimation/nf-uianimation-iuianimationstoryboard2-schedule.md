---
UID: NF:uianimation.IUIAnimationStoryboard2.Schedule
title: IUIAnimationStoryboard2::Schedule (uianimation.h)
description: Directs the storyboard to schedule itself for play. (IUIAnimationStoryboard2.Schedule)
helpviewer_keywords: ["IUIAnimationStoryboard2 interface [Windows Animation]","Schedule method","IUIAnimationStoryboard2.Schedule","IUIAnimationStoryboard2::Schedule","Schedule","Schedule method [Windows Animation]","Schedule method [Windows Animation]","IUIAnimationStoryboard2 interface","uianimation.iuianimationstoryboard2_schedule","uianimation/IUIAnimationStoryboard2::Schedule"]
old-location: uianimation\iuianimationstoryboard2_schedule.htm
tech.root: UIAnimation
ms.assetid: 9F20AE4A-F693-4DDA-90F4-FCCA5291208B
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard2 interface [Windows Animation],Schedule method, IUIAnimationStoryboard2.Schedule, IUIAnimationStoryboard2::Schedule, Schedule, Schedule method [Windows Animation], Schedule method [Windows Animation],IUIAnimationStoryboard2 interface, uianimation.iuianimationstoryboard2_schedule, uianimation/IUIAnimationStoryboard2::Schedule
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationStoryboard2::Schedule
 - uianimation/IUIAnimationStoryboard2::Schedule
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
 - IUIAnimationStoryboard2.Schedule
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

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

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
If the storyboard does not have priority, the attempt fails and the <i>schedulingResult</i> parameter is set to <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_scheduling_result">UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY</a>.

</li>
</ul>
If this method is called from a handler for <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">OnStoryboardStatusChanged</a> events, the <i>schedulingResult</i> parameter is set to <b>UI_ANIMATION_SCHEDULING_DEFERRED</b>.  The only way to determine whether the storyboard is successfully scheduled is to set a storyboard event handler and check whether the storyboard's status ever becomes <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_scheduling_result">UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY</a>.

It is possible to reuse a storyboard by calling <b>Schedule</b> again after its status has reached <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_READY</a>.  An attempt to schedule a storyboard when it is in any state other than <b>UI_ANIMATION_STORYBOARD_BUILDING</b> or <b>UI_ANIMATION_STORYBOARD_READY</b> fails, and  <i>schedulingResult</i> is set to <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_scheduling_result">UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-abandon">IUIAnimationStoryboard2::Abandon</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-conclude">IUIAnimationStoryboard2::Conclude</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-finish">IUIAnimationStoryboard2::Finish</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-getstatus">IUIAnimationStoryboard2::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-gettime">IUIAnimationTimer::GetTime</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_scheduling_result">UI_ANIMATION_SCHEDULING_RESULT</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
