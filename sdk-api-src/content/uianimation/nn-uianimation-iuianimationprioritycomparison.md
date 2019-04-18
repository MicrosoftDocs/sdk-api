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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationPriorityComparison interface


## -description


Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationPriorityComparison</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationPriorityComparison</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/82a90bd1-7bcf-4849-bad1-bae425169a2f">HasPriority</a>
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
         
         To determine which storyboard has priority, the animation manager can call <a href="https://msdn.microsoft.com/82a90bd1-7bcf-4849-bad1-bae425169a2f">HasPriority</a> on one or more  priority comparison handlers provided by the application.




## -see-also




<a href="https://msdn.microsoft.com/cea146d1-4a9c-4089-8015-ac16602f5afd">IUIAnimationManager::SetCancelPriorityComparison</a>



<a href="https://msdn.microsoft.com/bf2a7782-3541-483e-8d5e-3e82693f103c">IUIAnimationManager::SetCompressPriorityComparison</a>



<a href="https://msdn.microsoft.com/00a3d7e4-7ad2-46a8-a9c2-0e725005c00b">IUIAnimationManager::SetConcludePriorityComparison</a>



<a href="https://msdn.microsoft.com/f4c81cc4-4c00-4f78-819d-55f79972fe46">IUIAnimationManager::SetTrimPriorityComparison</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

