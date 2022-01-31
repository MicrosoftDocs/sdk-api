---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0002_0001
title: UI_ANIMATION_STORYBOARD_STATUS (uianimation.h)
description: Defines the status for a storyboard.
helpviewer_keywords: ["UI_ANIMATION_STORYBOARD_BUILDING","UI_ANIMATION_STORYBOARD_CANCELLED","UI_ANIMATION_STORYBOARD_FINISHED","UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY","UI_ANIMATION_STORYBOARD_PLAYING","UI_ANIMATION_STORYBOARD_READY","UI_ANIMATION_STORYBOARD_SCHEDULED","UI_ANIMATION_STORYBOARD_STATUS","UI_ANIMATION_STORYBOARD_STATUS enumeration [Windows Animation]","UI_ANIMATION_STORYBOARD_TRUNCATED","uianimation.ui_animation_storyboard_status","uianimation/UI_ANIMATION_STORYBOARD_BUILDING","uianimation/UI_ANIMATION_STORYBOARD_CANCELLED","uianimation/UI_ANIMATION_STORYBOARD_FINISHED","uianimation/UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY","uianimation/UI_ANIMATION_STORYBOARD_PLAYING","uianimation/UI_ANIMATION_STORYBOARD_READY","uianimation/UI_ANIMATION_STORYBOARD_SCHEDULED","uianimation/UI_ANIMATION_STORYBOARD_STATUS","uianimation/UI_ANIMATION_STORYBOARD_TRUNCATED"]
old-location: uianimation\ui_animation_storyboard_status.htm
tech.root: UIAnimation
ms.assetid: 02830092-0070-44dc-8db2-239941134473
ms.date: 12/05/2018
ms.keywords: UI_ANIMATION_STORYBOARD_BUILDING, UI_ANIMATION_STORYBOARD_CANCELLED, UI_ANIMATION_STORYBOARD_FINISHED, UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY, UI_ANIMATION_STORYBOARD_PLAYING, UI_ANIMATION_STORYBOARD_READY, UI_ANIMATION_STORYBOARD_SCHEDULED, UI_ANIMATION_STORYBOARD_STATUS, UI_ANIMATION_STORYBOARD_STATUS enumeration [Windows Animation], UI_ANIMATION_STORYBOARD_TRUNCATED, uianimation.ui_animation_storyboard_status, uianimation/UI_ANIMATION_STORYBOARD_BUILDING, uianimation/UI_ANIMATION_STORYBOARD_CANCELLED, uianimation/UI_ANIMATION_STORYBOARD_FINISHED, uianimation/UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY, uianimation/UI_ANIMATION_STORYBOARD_PLAYING, uianimation/UI_ANIMATION_STORYBOARD_READY, uianimation/UI_ANIMATION_STORYBOARD_SCHEDULED, uianimation/UI_ANIMATION_STORYBOARD_STATUS, uianimation/UI_ANIMATION_STORYBOARD_TRUNCATED
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
req.typenames: UI_ANIMATION_STORYBOARD_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_UIAnimation_0000_0002_0001
 - uianimation/__MIDL___MIDL_itf_UIAnimation_0000_0002_0001
 - UI_ANIMATION_STORYBOARD_STATUS
 - uianimation/UI_ANIMATION_STORYBOARD_STATUS
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
 - UI_ANIMATION_STORYBOARD_STATUS
---

# UI_ANIMATION_STORYBOARD_STATUS enumeration


## -description

Defines  the status for a storyboard.

## -enum-fields

### -field UI_ANIMATION_STORYBOARD_BUILDING:0

The storyboard has never been scheduled.

### -field UI_ANIMATION_STORYBOARD_SCHEDULED:1

The storyboard is scheduled to play.

### -field UI_ANIMATION_STORYBOARD_CANCELLED:2

The storyboard was canceled.

### -field UI_ANIMATION_STORYBOARD_PLAYING:3

The storyboard is currently playing.

### -field UI_ANIMATION_STORYBOARD_TRUNCATED:4

The storyboard was truncated.

### -field UI_ANIMATION_STORYBOARD_FINISHED:5

The storyboard has finished playing.

### -field UI_ANIMATION_STORYBOARD_READY:6

The storyboard is built and ready for scheduling.

### -field UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY:7

Scheduling the storyboard failed because a scheduling conflict occurred and the currently scheduled storyboard has higher priority.

## -remarks

Unless <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a> is called from a handler for <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">OnStoryboardStatusChanged</a> events, it returns only the following status values:

<ul>
<li>UI_ANIMATION_STORYBOARD_BUILDING</li>
<li>UI_ANIMATION_STORYBOARD_SCHEDULED</li>
<li>UI_ANIMATION_STORYBOARD_PLAYING</li>
<li>UI_ANIMATION_STORYBOARD_READY</li>
</ul>
All status values can be passed to  <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged</a>.

The following diagram illustrates the transitions between these states.

<img alt="Diagram that shows how the animation manager schedules the storyboard and manages the animation." src="images/StateDiagram.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged</a>
