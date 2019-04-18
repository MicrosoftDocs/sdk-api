---
UID: NF:uianimation.IUIAnimationManager.ScheduleTransition
title: IUIAnimationManager::ScheduleTransition (uianimation.h)
author: windows-sdk-content
description: Creates and schedules a single-transition storyboard.
old-location: uianimation\iuianimationmanager_scheduletransition.htm
tech.root: UIAnimation
ms.assetid: 0178b674-2ad3-49ee-92ce-925840ab8409
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],ScheduleTransition method, IUIAnimationManager.ScheduleTransition, IUIAnimationManager::ScheduleTransition, ScheduleTransition, ScheduleTransition method [Windows Animation], ScheduleTransition method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_scheduletransition, uianimation/IUIAnimationManager::ScheduleTransition
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationManager.ScheduleTransition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




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




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/32654e4b-158b-4d1a-afc7-98f90212b33b">IUIAnimationTimer::GetTime</a>



<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>



<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>
 

 

