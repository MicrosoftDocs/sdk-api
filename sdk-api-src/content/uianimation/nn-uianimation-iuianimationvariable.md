---
UID: NN:uianimation.IUIAnimationVariable
title: IUIAnimationVariable (uianimation.h)
author: windows-sdk-content
description: Defines an animation variable, which represents a visual element that can be animated.
old-location: uianimation\iuianimationvariable.htm
tech.root: UIAnimation
ms.assetid: 1632e62d-6e82-4841-8823-f6b60efc4298
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable, IUIAnimationVariable interface [Windows Animation], IUIAnimationVariable interface [Windows Animation],described, uianimation.iuianimationvariable, uianimation/IUIAnimationVariable
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationVariable"
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
 - IUIAnimationVariable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationVariable interface


## -description


Defines an animation variable, which represents a visual element that can be animated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getcurrentstoryboard">GetCurrentStoryboard</a>
</td>
<td align="left" width="63%">
Gets the storyboard that is currently animating the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalintegervalue">GetFinalIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the final value of the animation variable as an integer.      
         

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalvalue">GetFinalValue</a>
</td>
<td align="left" width="63%">
Gets the final value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">GetIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the current value of the animation variable as an integer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">GetPreviousIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the previous value of the animation variable as an integer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousvalue">GetPreviousValue</a>
</td>
<td align="left" width="63%">
Gets the previous value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag for an animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Gets the current value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setlowerbound">SetLowerBound</a>
</td>
<td align="left" width="63%">
Sets the lower bound (floor) for the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setroundingmode">SetRoundingMode</a>
</td>
<td align="left" width="63%">
Specifies the rounding mode for the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-settag">SetTag</a>
</td>
<td align="left" width="63%">
Sets the tag for an animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setupperbound">SetUpperBound</a>
</td>
<td align="left" width="63%">
Sets the upper bound (ceiling) for the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariablechangehandler">SetVariableChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies a variable change handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler">SetVariableIntegerChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies an integer variable change handler.

</td>
</tr>
</table> 


## -remarks



Along with 
         <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a> and 
         <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>, <b>IUIAnimationVariable</b> is a primary component for building animations. To create and manage animation variables, use <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-createanimationvariable">IUIAnimationManager::CreateAnimationVariable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getvariablefromtag">IUIAnimationManager::GetVariableFromTag</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-scheduletransition">IUIAnimationManager::ScheduleTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-holdvariable">IUIAnimationStoryboard::HoldVariable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

