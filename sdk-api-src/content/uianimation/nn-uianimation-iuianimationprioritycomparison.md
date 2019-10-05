---
UID: NN:uianimation.IUIAnimationPriorityComparison
title: IUIAnimationPriorityComparison (uianimation.h)
author: windows-sdk-content
description: Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.
old-location: uianimation\iuianimationprioritycomparison.htm
tech.root: UIAnimation
ms.assetid: 65311cf0-f8d4-4d2c-bd4d-585ae5d921df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationPriorityComparison, IUIAnimationPriorityComparison interface [Windows Animation], IUIAnimationPriorityComparison interface [Windows Animation],described, uianimation.iuianimationprioritycomparison, uianimation/IUIAnimationPriorityComparison
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationPriorityComparison"
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
 - IUIAnimationPriorityComparison
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationPriorityComparison interface


## -description


Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationPriorityComparison</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationPriorityComparison</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationPriorityComparison</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationprioritycomparison-haspriority">HasPriority</a>
</td>
<td align="left" width="63%">
Determines the relative priority between a scheduled storyboard and a new storyboard.

</td>
</tr>
</table> 


## -remarks



A single animation variable can be included in multiple storyboards, 
         but multiple storyboards cannot animate the same variable at the same time.
         
         If a newly scheduled storyboard attempts to animate one or more variables that are currently scheduled for animation by  different storyboards, a scheduling conflict occurs.
         
         To determine which storyboard has priority, the animation manager can call <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationprioritycomparison-haspriority">HasPriority</a> on one or more  priority comparison handlers provided by the application.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcancelprioritycomparison">IUIAnimationManager::SetCancelPriorityComparison</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcompressprioritycomparison">IUIAnimationManager::SetCompressPriorityComparison</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setconcludeprioritycomparison">IUIAnimationManager::SetConcludePriorityComparison</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-settrimprioritycomparison">IUIAnimationManager::SetTrimPriorityComparison</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

