---
UID: NF:uianimation.IUIAnimationTimer.IsEnabled
title: IUIAnimationTimer::IsEnabled (uianimation.h)
description: Determines whether the timer is currently enabled.
helpviewer_keywords: ["IUIAnimationTimer interface [Windows Animation]","IsEnabled method","IUIAnimationTimer.IsEnabled","IUIAnimationTimer::IsEnabled","IsEnabled","IsEnabled method [Windows Animation]","IsEnabled method [Windows Animation]","IUIAnimationTimer interface","uianimation.iuianimationtimer_isenabled","uianimation/IUIAnimationTimer::IsEnabled"]
old-location: uianimation\iuianimationtimer_isenabled.htm
tech.root: UIAnimation
ms.assetid: 42a7e690-40bb-4795-9076-5e4bed62562d
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimer interface [Windows Animation],IsEnabled method, IUIAnimationTimer.IsEnabled, IUIAnimationTimer::IsEnabled, IsEnabled, IsEnabled method [Windows Animation], IsEnabled method [Windows Animation],IUIAnimationTimer interface, uianimation.iuianimationtimer_isenabled, uianimation/IUIAnimationTimer::IsEnabled
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
 - IUIAnimationTimer::IsEnabled
 - uianimation/IUIAnimationTimer::IsEnabled
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
 - IUIAnimationTimer.IsEnabled
---

# IUIAnimationTimer::IsEnabled


## -description

Determines whether the timer is currently enabled.



## -returns

Returns S_OK if the animation timer is enabled, S_FALSE if the animation timer is disabled, or an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-disable">IUIAnimationTimer::Disable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-enable">IUIAnimationTimer::Enable</a>
