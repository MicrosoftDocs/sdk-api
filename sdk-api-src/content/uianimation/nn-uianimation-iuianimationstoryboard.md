---
UID: NN:uianimation.IUIAnimationStoryboard
title: IUIAnimationStoryboard (uianimation.h)
author: windows-sdk-content
description: Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.
old-location: uianimation\iuianimationstoryboard.htm
tech.root: UIAnimation
ms.assetid: 6b30b660-dfa4-410f-a8de-58ea5c9a104d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard, IUIAnimationStoryboard interface [Windows Animation], IUIAnimationStoryboard interface [Windows Animation],described, uianimation.iuianimationstoryboard, uianimation/IUIAnimationStoryboard
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationStoryboard"
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
 - IUIAnimationStoryboard
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationStoryboard interface


## -description


Defines a storyboard, which contains a group of transitions
      that are synchronized relative to one another.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationStoryboard</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationStoryboard</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationStoryboard</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-abandon">Abandon</a>
</td>
<td align="left" width="63%">
Directs the storyboard to abandon playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">AddKeyframeAfterTransition</a>
</td>
<td align="left" width="63%">
Adds a keyfame at the end of the specified transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset">AddKeyframeAtOffset</a>
</td>
<td align="left" width="63%">
Adds a keyfame at the specified offset from an existing keyframe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">AddTransition</a>
</td>
<td align="left" width="63%">
Adds a transition to the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">AddTransitionAtKeyframe</a>
</td>
<td align="left" width="63%">
Adds a transition that starts at the specified keyframe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">AddTransitionBetweenKeyframes</a>
</td>
<td align="left" width="63%">
Adds a transition between two keyframes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-conclude">Conclude</a>
</td>
<td align="left" width="63%">
Directs the storyboard to conclude.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-finish">Finish</a>
</td>
<td align="left" width="63%">
Directs the storyboard to finish playing within the specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getelapsedtime">GetElapsedTime</a>
</td>
<td align="left" width="63%">
Gets the time elapsed since the storyboard started playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag for the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-holdvariable">HoldVariable</a>
</td>
<td align="left" width="63%">
Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-repeatbetweenkeyframes">RepeatBetweenKeyframes</a>
</td>
<td align="left" width="63%">
Creates a loop between two specified keyframes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-schedule">Schedule</a>
</td>
<td align="left" width="63%">
Directs the storyboard to schedule itself for play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay">SetLongestAcceptableDelay</a>
</td>
<td align="left" width="63%">
Sets the longest acceptable delay before the scheduled storyboard begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setstoryboardeventhandler">SetStoryboardEventHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for storyboard events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-settag">SetTag</a>
</td>
<td align="left" width="63%">
Sets the tag for the storyboard.

</td>
</tr>
</table> 


## -remarks



<b>IUIAnimationStoryboard</b> is a primary component for building animations,
         along with 
         <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a> and 
         <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>.
         
         




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-abandonallstoryboards">IUIAnimationManager::AbandonAllStoryboards</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-createstoryboard">IUIAnimationManager::CreateStoryboard</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-finishallstoryboards">IUIAnimationManager::FinishAllStoryboards</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstoryboardfromtag">IUIAnimationManager::GetStoryboardFromTag</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getcurrentstoryboard">IUIAnimationVariable::GetCurrentStoryboard</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/storyboard-construction">Storyboard Overview</a>
 

 

