---
UID: NN:uianimation.IUIAnimationLoopIterationChangeHandler2
title: IUIAnimationLoopIterationChangeHandler2
author: windows-driver-content
description: Defines a method for handling storyboard loop iteration events.
old-location: uianimation\iuianimationloopiterationchangehandler2.htm
old-project: UIAnimation
ms.assetid: DB3995BA-856F-407D-AA89-247D84C3F7A1
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IUIAnimationLoopIterationChangeHandler2, IUIAnimationLoopIterationChangeHandler2 interface [Windows Animation], IUIAnimationLoopIterationChangeHandler2 interface [Windows Animation],described, uianimation.iuianimationloopiterationchangehandler2, uianimation/IUIAnimationLoopIterationChangeHandler2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationLoopIterationChangeHandler2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationLoopIterationChangeHandler2 interface


## -description


Defines a method for handling storyboard loop iteration events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationLoopIterationChangeHandler2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationLoopIterationChangeHandler2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationLoopIterationChangeHandler2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C441CDC6-944E-488A-B643-13A13E027DF6">OnLoopIterationChanged</a>
</td>
<td align="left" width="63%">
Handles loop iteration change events, which occur when a loop within a storyboard begins a new iteration.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/d37718ac-0256-4a24-a26c-d29173593be0">Storyboard Overview</a>
 

 

