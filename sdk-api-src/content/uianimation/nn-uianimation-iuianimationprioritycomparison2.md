---
UID: NN:uianimation.IUIAnimationPriorityComparison2
title: IUIAnimationPriorityComparison2 (uianimation.h)
description: Defines a method that resolves scheduling conflicts through priority comparison.
helpviewer_keywords: ["IUIAnimationPriorityComparison2","IUIAnimationPriorityComparison2 interface [Windows Animation]","IUIAnimationPriorityComparison2 interface [Windows Animation]","described","uianimation.iuianimationprioritycomparison2","uianimation/IUIAnimationPriorityComparison2"]
old-location: uianimation\iuianimationprioritycomparison2.htm
tech.root: UIAnimation
ms.assetid: B19E9BAF-A91E-4A58-A6F0-058B03153D10
ms.date: 12/05/2018
ms.keywords: IUIAnimationPriorityComparison2, IUIAnimationPriorityComparison2 interface [Windows Animation], IUIAnimationPriorityComparison2 interface [Windows Animation],described, uianimation.iuianimationprioritycomparison2, uianimation/IUIAnimationPriorityComparison2
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
 - IUIAnimationPriorityComparison2
 - uianimation/IUIAnimationPriorityComparison2
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
 - IUIAnimationPriorityComparison2
---

# IUIAnimationPriorityComparison2 interface


## -description

Defines a method that resolves scheduling conflicts through priority comparison.

## -inheritance

The <b>IUIAnimationPriorityComparison2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationPriorityComparison2</b> also has these types of members:

## -remarks

A single animation variable can be included in multiple storyboards, but multiple storyboards cannot animate the same variable at the same time.
         
If a newly scheduled storyboard attempts to animate one or more variables that are currently scheduled for animation by  different storyboards, a scheduling conflict occurs.
         
To determine which storyboard has priority, the animation manager can call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationprioritycomparison2-haspriority">HasPriority</a> method on one or more  priority comparison handlers provided by the application.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setcancelprioritycomparison">IUIAnimationManager2::SetCancelPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setcompressprioritycomparison">IUIAnimationManager2::SetCompressPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setconcludeprioritycomparison">IUIAnimationManager2::SetConcludePriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-settrimprioritycomparison">IUIAnimationManager2::SetTrimPriorityComparison</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
