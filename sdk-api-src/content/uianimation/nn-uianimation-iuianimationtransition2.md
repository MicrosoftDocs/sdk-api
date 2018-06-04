---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

