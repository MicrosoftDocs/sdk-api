---
UID: NF:uianimation.IUIAnimationManager2.ScheduleTransition
title: IUIAnimationManager2::ScheduleTransition (uianimation.h)
author: windows-sdk-content
description: Creates and schedules a single-transition storyboard.
old-location: uianimation\iuianimationmanager2_scheduletransition.htm
tech.root: UIAnimation
ms.assetid: F0F5D099-6290-485F-AD68-101CD57E8656
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],ScheduleTransition method, IUIAnimationManager2.ScheduleTransition, IUIAnimationManager2::ScheduleTransition, ScheduleTransition, ScheduleTransition method [Windows Animation], ScheduleTransition method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_scheduletransition, uianimation/IUIAnimationManager2::ScheduleTransition
ms.topic: method
f1_keywords: 
 - "uianimation/IUIAnimationManager2.ScheduleTransition"
dev_langs:
 - c++
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
 - IUIAnimationManager2.ScheduleTransition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationManager2::ScheduleTransition


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



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method schedules a new storyboard by creating the storyboard, applying the specified transition to the specified variable, and then scheduling the storyboard.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-gettime">IUIAnimationTimer::GetTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>
 

 

