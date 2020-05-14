---
UID: NF:uianimation.IUIAnimationTimer.GetTime
title: IUIAnimationTimer::GetTime (uianimation.h)
description: Gets the current time.helpviewer_keywords: ["GetTime","GetTime method [Windows Animation]","GetTime method [Windows Animation]","IUIAnimationTimer interface","IUIAnimationTimer interface [Windows Animation]","GetTime method","IUIAnimationTimer.GetTime","IUIAnimationTimer::GetTime","uianimation.iuianimationtimer_gettime","uianimation/IUIAnimationTimer::GetTime"]
old-location: uianimation\iuianimationtimer_gettime.htm
tech.root: UIAnimation
ms.assetid: 32654e4b-158b-4d1a-afc7-98f90212b33b
ms.date: 12/05/2018
ms.keywords: GetTime, GetTime method [Windows Animation], GetTime method [Windows Animation],IUIAnimationTimer interface, IUIAnimationTimer interface [Windows Animation],GetTime method, IUIAnimationTimer.GetTime, IUIAnimationTimer::GetTime, uianimation.iuianimationtimer_gettime, uianimation/IUIAnimationTimer::GetTime
f1_keywords:
- uianimation/IUIAnimationTimer.GetTime
dev_langs:
- c++
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
- IUIAnimationTimer.GetTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTimer::GetTime


## -description


Gets the current time.


## -parameters




### -param seconds [out]

The current time, in <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method can be used in both the application-driven and timer-driven  configurations to retrieve the system time in <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>, the units used throughout the Windows Animation API.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/introducing-windows-animation-manager">Update the Animation Manager and Draw Frames</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>
 

 

