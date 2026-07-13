---
UID: NN:uianimation.IUIAnimationPriorityComparison
title: IUIAnimationPriorityComparison (uianimation.h)
description: Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.
helpviewer_keywords: ["IUIAnimationPriorityComparison","IUIAnimationPriorityComparison interface [Windows Animation]","IUIAnimationPriorityComparison interface [Windows Animation]","described","uianimation.iuianimationprioritycomparison","uianimation/IUIAnimationPriorityComparison"]
old-location: uianimation\iuianimationprioritycomparison.htm
tech.root: UIAnimation
ms.assetid: 65311cf0-f8d4-4d2c-bd4d-585ae5d921df
ms.date: 12/05/2018
ms.keywords: IUIAnimationPriorityComparison, IUIAnimationPriorityComparison interface [Windows Animation], IUIAnimationPriorityComparison interface [Windows Animation],described, uianimation.iuianimationprioritycomparison, uianimation/IUIAnimationPriorityComparison
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
 - IUIAnimationPriorityComparison
 - uianimation/IUIAnimationPriorityComparison
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
 - IUIAnimationPriorityComparison
---

# IUIAnimationPriorityComparison interface


## -description

Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.

## -inheritance

The <b>IUIAnimationPriorityComparison</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationPriorityComparison</b> also has these types of members:

## -remarks

A single animation variable can be included in multiple storyboards, but multiple storyboards cannot animate the same variable at the same time.
         
If a newly scheduled storyboard attempts to animate one or more variables that are currently scheduled for animation by  different storyboards, a scheduling conflict occurs.
         
To determine which storyboard has priority, the animation manager can call <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationprioritycomparison-haspriority">HasPriority</a> on one or more  priority comparison handlers provided by the application.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcancelprioritycomparison">IUIAnimationManager::SetCancelPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcompressprioritycomparison">IUIAnimationManager::SetCompressPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setconcludeprioritycomparison">IUIAnimationManager::SetConcludePriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-settrimprioritycomparison">IUIAnimationManager::SetTrimPriorityComparison</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
