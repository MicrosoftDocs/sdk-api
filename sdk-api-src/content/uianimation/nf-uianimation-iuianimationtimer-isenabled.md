---
UID: NF:uianimation.IUIAnimationTimer.IsEnabled
title: IUIAnimationTimer::IsEnabled
author: windows-driver-content
description: Determines whether the timer is currently enabled.
old-location: uianimation\iuianimationtimer_isenabled.htm
old-project: UIAnimation
ms.assetid: 42a7e690-40bb-4795-9076-5e4bed62562d
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IUIAnimationTimer interface [Windows Animation],IsEnabled method, IUIAnimationTimer.IsEnabled, IUIAnimationTimer::IsEnabled, IsEnabled, IsEnabled method [Windows Animation], IsEnabled method [Windows Animation],IUIAnimationTimer interface, uianimation.iuianimationtimer_isenabled, uianimation/IUIAnimationTimer::IsEnabled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTimer.IsEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTimer::IsEnabled


## -description



      Determines whether the timer is currently enabled.


## -parameters






## -returns




               Returns S_OK if the animation timer is enabled, S_FALSE if the animation timer is disabled, or an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">IUIAnimationTimer</a>



<a href="https://msdn.microsoft.com/981f2086-3588-4150-aa0a-c427b93ef8bb">
      IUIAnimationTimer::Disable</a>



<a href="https://msdn.microsoft.com/b2efd694-67ff-4e6e-9a47-d0ce70dbd85a">
      IUIAnimationTimer::Enable</a>
 

 

