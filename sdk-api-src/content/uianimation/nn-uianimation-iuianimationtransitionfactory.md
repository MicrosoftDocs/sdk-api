---
UID: NN:uianimation.IUIAnimationTransitionFactory
title: IUIAnimationTransitionFactory
author: windows-sdk-content
description: Defines a method for creating transitions from custom interpolators.
old-location: uianimation\iuianimationtransitionfactory.htm
old-project: UIAnimation
ms.assetid: 62aec8da-e067-4b61-9465-e07fb5b42b7f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationTransitionFactory, IUIAnimationTransitionFactory interface [Windows Animation], IUIAnimationTransitionFactory interface [Windows Animation],described, uianimation.iuianimationtransitionfactory, uianimation/IUIAnimationTransitionFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uianimation.h
req.include-header: 
req.redist: 
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
 - IUIAnimationTransitionFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionFactory interface


## -description


Defines a method for creating transitions from custom interpolators.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTransitionFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTransitionFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTransitionFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02d28669-0cbd-41e2-b9ca-4ad893f09fc9">CreateTransition</a>
</td>
<td align="left" width="63%">
Creates a transition from a custom interpolator.

</td>
</tr>
</table> 


## -remarks



When an application requires animation effects that are not available in the transition library, developers can implement custom transitions that it can use. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from the interpolator. An interpolator must implement the <a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>interface; an implementation of the transition factory object is provided by <a href="https://msdn.microsoft.com/27749b03-e993-42bf-855d-4fe352a1bb8e">UIAnimationTransitionFactory</a>.




## -see-also




<a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

