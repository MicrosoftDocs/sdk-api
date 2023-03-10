---
UID: NF:uianimation.IUIAnimationManager.ScheduleTransition
title: IUIAnimationManager::ScheduleTransition (uianimation.h)
description: Creates and schedules a single-transition storyboard. (IUIAnimationManager.ScheduleTransition)
helpviewer_keywords: ["IUIAnimationManager interface [Windows Animation]","ScheduleTransition method","IUIAnimationManager.ScheduleTransition","IUIAnimationManager::ScheduleTransition","ScheduleTransition","ScheduleTransition method [Windows Animation]","ScheduleTransition method [Windows Animation]","IUIAnimationManager interface","uianimation.iuianimationmanager_scheduletransition","uianimation/IUIAnimationManager::ScheduleTransition"]
old-location: uianimation\iuianimationmanager_scheduletransition.htm
tech.root: UIAnimation
ms.assetid: 0178b674-2ad3-49ee-92ce-925840ab8409
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],ScheduleTransition method, IUIAnimationManager.ScheduleTransition, IUIAnimationManager::ScheduleTransition, ScheduleTransition, ScheduleTransition method [Windows Animation], ScheduleTransition method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_scheduletransition, uianimation/IUIAnimationManager::ScheduleTransition
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
 - IUIAnimationManager::ScheduleTransition
 - uianimation/IUIAnimationManager::ScheduleTransition
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
 - IUIAnimationManager.ScheduleTransition
---

# IUIAnimationManager::ScheduleTransition


## -description

Creates and schedules a single-transition storyboard.

## -parameters

### -param variable [in]

The animation variable.

### -param transition [in]

A transition to be applied to the animation variable.

### -param timeNow [in]

The current system time.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method schedules a new storyboard by creating the storyboard, applying the specified transition to the specified variable, and then scheduling the storyboard.


#### Examples

The following example creates a storyboard for a specified transition and animation variable.


```cpp
// Get the current time and schedule a single-transition storyboard

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->ScheduleTransition(
        m_pAnimationVariableY,
        pTransitionParabolic,
        secondsNow
        );
    ...
}

```

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-gettime">IUIAnimationTimer::GetTime</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>
