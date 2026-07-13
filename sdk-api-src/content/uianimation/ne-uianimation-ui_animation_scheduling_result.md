---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0002_0002
title: UI_ANIMATION_SCHEDULING_RESULT (uianimation.h)
description: Defines results for storyboard scheduling.
helpviewer_keywords: ["UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED","UI_ANIMATION_SCHEDULING_DEFERRED","UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY","UI_ANIMATION_SCHEDULING_RESULT","UI_ANIMATION_SCHEDULING_RESULT enumeration [Windows Animation]","UI_ANIMATION_SCHEDULING_SUCCEEDED","UI_ANIMATION_SCHEDULING_UNEXPECTED_FAILURE","uianimation.ui_animation_scheduling_result","uianimation/UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED","uianimation/UI_ANIMATION_SCHEDULING_DEFERRED","uianimation/UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY","uianimation/UI_ANIMATION_SCHEDULING_RESULT","uianimation/UI_ANIMATION_SCHEDULING_SUCCEEDED","uianimation/UI_ANIMATION_SCHEDULING_UNEXPECTED_FAILURE"]
old-location: uianimation\ui_animation_scheduling_result.htm
tech.root: UIAnimation
ms.assetid: 2d62589a-9121-4af6-b704-566a28dcc21e
ms.date: 12/05/2018
ms.keywords: UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED, UI_ANIMATION_SCHEDULING_DEFERRED, UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY, UI_ANIMATION_SCHEDULING_RESULT, UI_ANIMATION_SCHEDULING_RESULT enumeration [Windows Animation], UI_ANIMATION_SCHEDULING_SUCCEEDED, UI_ANIMATION_SCHEDULING_UNEXPECTED_FAILURE, uianimation.ui_animation_scheduling_result, uianimation/UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED, uianimation/UI_ANIMATION_SCHEDULING_DEFERRED, uianimation/UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY, uianimation/UI_ANIMATION_SCHEDULING_RESULT, uianimation/UI_ANIMATION_SCHEDULING_SUCCEEDED, uianimation/UI_ANIMATION_SCHEDULING_UNEXPECTED_FAILURE
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
targetos: Windows
req.typenames: UI_ANIMATION_SCHEDULING_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_UIAnimation_0000_0002_0002
 - uianimation/__MIDL___MIDL_itf_UIAnimation_0000_0002_0002
 - UI_ANIMATION_SCHEDULING_RESULT
 - uianimation/UI_ANIMATION_SCHEDULING_RESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAnimation.h
api_name:
 - UI_ANIMATION_SCHEDULING_RESULT
---

# UI_ANIMATION_SCHEDULING_RESULT enumeration


## -description

Defines results for storyboard scheduling.

## -enum-fields

### -field UI_ANIMATION_SCHEDULING_UNEXPECTED_FAILURE:0

Scheduling failed for an unexpected reason.

### -field UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY:1

Scheduling failed because
               a scheduling conflict occurred and the currently scheduled storyboard has higher priority.
               
               For more information, see <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationprioritycomparison-haspriority">IUIAnimationPriorityComparison::HasPriority</a>.

### -field UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED:2

Scheduling failed because 
               the storyboard is already scheduled.

### -field UI_ANIMATION_SCHEDULING_SUCCEEDED:3

Scheduling succeeded.

### -field UI_ANIMATION_SCHEDULING_DEFERRED:4

Scheduling is deferred and will be attempted when the current callback completes.

## -remarks

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-schedule">IUIAnimationStoryboard::Schedule</a> returns UI_ANIMATION_SCHEDULING_DEFERRED only if the application attempts to schedule a storyboard during a callback to <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-schedule">IUIAnimationStoryboard::Schedule</a>
