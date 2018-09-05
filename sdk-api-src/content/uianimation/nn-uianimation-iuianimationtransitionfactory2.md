---
UID: NN:uianimation.IUIAnimationTransitionFactory2
title: IUIAnimationTransitionFactory2
author: windows-sdk-content
description: Defines a method for creating transitions from custom interpolators. supports the creation of transitions in a specified dimension.
old-location: uianimation\iuianimationtransitionfactory2.htm
old-project: UIAnimation
ms.assetid: EB829B6A-770C-486A-9BA2-4D7C8F073C8F
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationTransitionFactory2, IUIAnimationTransitionFactory2 interface [Windows Animation], IUIAnimationTransitionFactory2 interface [Windows Animation],described, uianimation.iuianimationtransitionfactory2, uianimation/IUIAnimationTransitionFactory2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uianimation.h
req.include-header: 
req.redist: 
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
 - IUIAnimationTransitionFactory2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionFactory2 interface


## -description


Defines a method for creating transitions from custom interpolators.

<b>IUIAnimationTransitionFactory2</b> supports the creation of transitions in a specified dimension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTransitionFactory2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTransitionFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTransitionFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CFF79A6B-B2C1-4B48-8F1E-70ED2CBC567A">CreateTransition</a>
</td>
<td align="left" width="63%">
Creates a transition from a custom interpolator for a given dimension.

</td>
</tr>
</table> 


## -remarks



When an application requires animation effects that are not available in the transition library, developers can implement custom transitions that the application can use. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from the interpolator. An interpolator must implement either the <a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>interface or the <a href="https://msdn.microsoft.com/EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04">IUIAnimationInterpolator2</a> interface; an implementation of the transition factory object is provided by <a href="https://msdn.microsoft.com/27749b03-e993-42bf-855d-4fe352a1bb8e">UIAnimationTransitionFactory</a> or by <a href="https://msdn.microsoft.com/4583920B-FF11-48C8-B311-66F5DE3F9D9C">UIAnimationTransitionFactory2</a>.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/b54e319c-e140-4fd9-8045-5eb6f4a31326">Interfaces</a>
 

 

