---
UID: NN:uianimation.IUIAnimationManager2
title: IUIAnimationManager2 (uianimation.h)
description: Defines an animation manager, which provides a central interface for creating and managing animations in multiple dimensions.
old-location: uianimation\iuianimationmanager2.htm
tech.root: UIAnimation
ms.assetid: BD7DAD23-2A7D-4EE7-9BCF-8380F928674D
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2, IUIAnimationManager2 interface [Windows Animation], IUIAnimationManager2 interface [Windows Animation],described, uianimation.iuianimationmanager2, uianimation/IUIAnimationManager2
ms.topic: interface
f1_keywords:
- uianimation/IUIAnimationManager2
dev_langs:
- c++
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
- IUIAnimationManager2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationManager2 interface


## -description


Defines an <b>animation manager</b>, which provides a central interface for creating and managing animations in multiple dimensions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationManager2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-abandonallstoryboards">AbandonAllStoryboards</a>
</td>
<td align="left" width="63%">
Abandons all active storyboards.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-createanimationvariable">CreateAnimationVariable</a>
</td>
<td align="left" width="63%">
Creates a new animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-createanimationvectorvariable">CreateAnimationVectorVariable</a>
</td>
<td align="left" width="63%">
Creates a new animation variable for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-createstoryboard">CreateStoryboard</a>
</td>
<td align="left" width="63%">
Creates a new storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-estimatenexteventtime">EstimateNextEventTime</a>
</td>
<td align="left" width="63%">
Retrieves an estimate of  the time interval before the next animation event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-finishallstoryboards">FinishAllStoryboards</a>
</td>
<td align="left" width="63%">
Finishes all active storyboards within the specified time interval.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the animation manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstoryboardfromtag">GetStoryboardFromTag</a>
</td>
<td align="left" width="63%">
Gets the storyboard with the specified tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getvariablefromtag">GetVariableFromTag</a>
</td>
<td align="left" width="63%">
Gets the animation variable with the specified tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses all animations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-resume">Resume</a>
</td>
<td align="left" width="63%">
Resumes all animations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-scheduletransition">ScheduleTransition</a>
</td>
<td align="left" width="63%">
Creates and schedules a single-transition storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setanimationmode">SetAnimationMode</a>
</td>
<td align="left" width="63%">
Sets the animation mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setcancelprioritycomparison">SetCancelPriorityComparison</a>
</td>
<td align="left" width="63%">
Sets the priority comparison handler that determines whether  a scheduled storyboard can be canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setcompressprioritycomparison">SetCompressPriorityComparison</a>
</td>
<td align="left" width="63%">
Sets the priority comparison handler that determines whether  a scheduled storyboard can be compressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setconcludeprioritycomparison">SetConcludePriorityComparison</a>
</td>
<td align="left" width="63%">
Sets the priority comparison handler that determines whether  a scheduled storyboard can be concluded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setdefaultlongestacceptabledelay">SetDefaultLongestAcceptableDelay</a>
</td>
<td align="left" width="63%">
Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setmanagereventhandler">SetManagerEventHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for animation manager status updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-settrimprioritycomparison">SetTrimPriorityComparison</a>
</td>
<td align="left" width="63%">
Sets the priority comparison handler that determines whether  a scheduled storyboard can be trimmed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the animation manager and all its associated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-update">Update</a>
</td>
<td align="left" width="63%">
Updates the values of all animation variables.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>
 

 

