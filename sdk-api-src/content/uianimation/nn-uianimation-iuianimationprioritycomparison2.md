---
UID: NN:uianimation.IUIAnimationPriorityComparison2
title: IUIAnimationPriorityComparison2
author: windows-sdk-content
description: Defines a method that resolves scheduling conflicts through priority comparison.
old-location: uianimation\iuianimationprioritycomparison2.htm
old-project: UIAnimation
ms.assetid: B19E9BAF-A91E-4A58-A6F0-058B03153D10
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IUIAnimationPriorityComparison2, IUIAnimationPriorityComparison2 interface [Windows Animation], IUIAnimationPriorityComparison2 interface [Windows Animation],described, uianimation.iuianimationprioritycomparison2, uianimation/IUIAnimationPriorityComparison2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationPriorityComparison2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationPriorityComparison2 interface


## -description


Defines a method that resolves scheduling conflicts through priority comparison.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationPriorityComparison2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationPriorityComparison2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationPriorityComparison2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A448144F-37B2-46E5-AA0D-604CE3FDEAA4">HasPriority</a>
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
         
         To determine which storyboard has priority, the animation manager can call the <a href="https://msdn.microsoft.com/A448144F-37B2-46E5-AA0D-604CE3FDEAA4">HasPriority</a> method on one or more  priority comparison handlers provided by the application.




## -see-also




<a href="https://msdn.microsoft.com/55DEC4C2-A6F3-459D-BDCD-3D3819EBF0D2">IUIAnimationManager2::SetCancelPriorityComparison</a>



<a href="https://msdn.microsoft.com/A754A307-AFFB-4E43-862D-C2FBC85E6C74">IUIAnimationManager2::SetCompressPriorityComparison</a>



<a href="https://msdn.microsoft.com/1BDC9094-6020-4640-B959-59CD6CF48751">IUIAnimationManager2::SetConcludePriorityComparison</a>



<a href="https://msdn.microsoft.com/742BCD19-FC1D-46DE-9CBC-716793259947">IUIAnimationManager2::SetTrimPriorityComparison</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

