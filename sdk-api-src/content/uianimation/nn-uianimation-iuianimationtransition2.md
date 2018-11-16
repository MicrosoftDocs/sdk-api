---
UID: NN:uianimation.IUIAnimationTransition2
title: IUIAnimationTransition2
author: windows-sdk-content
description: Extends the IUIAnimationTransition interface that defines a transition. An IUIAnimationTransition2 transition determines how an animation variable changes over time in a given dimension.
old-location: uianimation\iuianimationtransition2.htm
tech.root: UIAnimation
ms.assetid: CACB8053-7716-42E4-9C3B-9CCBBC30808A
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IUIAnimationTransition2, IUIAnimationTransition2 interface [Windows Animation], IUIAnimationTransition2 interface [Windows Animation],described, uianimation.iuianimationtransition2, uianimation/IUIAnimationTransition2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IUIAnimationTransition2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationTransition2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a> interface that defines a transition. An  <b>IUIAnimationTransition2</b> transition determines how an animation variable  changes over time in a given dimension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTransition2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTransition2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTransition2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0C5B6B70-B400-466E-BB6A-1BF9313C106D">GetDimension</a>
</td>
<td align="left" width="63%">
Gets the number of dimensions in which the animation variable has a transition specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07B5C7D7-80B1-4458-93A7-39F61121B618">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A73065A7-B191-4CB9-A75A-827CFC040C92">IsDurationKnown</a>
</td>
<td align="left" width="63%">
Determines whether the duration of a transition is known.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/813224BE-369D-4D65-AA12-AEE590627F40">SetInitialValue</a>
</td>
<td align="left" width="63%">
Sets the initial value of the transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B46F15F2-8C2A-4F15-9BBE-20FB8E5C84C6">SetInitialVectorValue</a>
</td>
<td align="left" width="63%">
Sets the initial value of the transition for each specified dimension in the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29EFBBE0-E877-4521-B4A7-E1828E0493B9">SetInitialVectorVelocity</a>
</td>
<td align="left" width="63%">
Sets the initial velocity of the transition for each specified dimension in the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1CE8A3BD-9DDC-4FDE-BE2B-29804B3754B1">SetInitialVelocity</a>
</td>
<td align="left" width="63%">
Sets the initial velocity of the transition.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/b54e319c-e140-4fd9-8045-5eb6f4a31326">Interfaces</a>
 

 

