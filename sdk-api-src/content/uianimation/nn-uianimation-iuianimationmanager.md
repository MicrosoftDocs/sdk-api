---
UID: NN:uianimation.IUIAnimationManager
title: IUIAnimationManager (uianimation.h)
author: windows-sdk-content
description: Defines the animation manager, which provides a central interface for creating and managing animations.
old-location: uianimation\iuianimationmanager.htm
tech.root: UIAnimation
ms.assetid: 21f16c65-90aa-4b1f-93bc-8ee0488c6ded
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager, IUIAnimationManager interface [Windows Animation], IUIAnimationManager interface [Windows Animation],described, uianimation.iuianimationmanager, uianimation/IUIAnimationManager
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationManager"
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
 - IUIAnimationManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationManager interface


## -description


Defines the animation manager, which provides a central interface for creating and managing animations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-abandonallstoryboards">AbandonAllStoryboards</a>
</td>
<td align="left" width="63%">
Abandons all active storyboards.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-createanimationvariable">CreateAnimationVariable</a>
</td>
<td align="left" width="63%">
Creates a new animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-createstoryboard">CreateStoryboard</a>
</td>
<td align="left" width="63%">
Creates a new storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-finishallstoryboards">FinishAllStoryboards</a>
</td>
<td align="left" width="63%">
Finishes all active storyboards within the specified time interval.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the animation manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstoryboardfromtag">GetStoryboardFromTag</a>
</td>
<td align="left" width="63%">
Gets the storyboard with the specified tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getvariablefromtag">GetVariableFromTag</a>
</td>
<td align="left" width="63%">
Gets the animation variable with the specified tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses all animations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-resume">Resume</a>
</td>
<td align="left" width="63%">
Resumes all animations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-scheduletransition">ScheduleTransition</a>
</td>
<td align="left" width="63%">
Creates and schedules a single-transition storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setanimationmode">SetAnimationMode</a>
</td>
<td align="left" width="63%">
Sets the animation mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcancelprioritycomparison">SetCancelPriorityComparison</a>
</td>
<td align="left" width="63%">
Sets a priority comparison handler for cancelation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcompressprioritycomparison">SetCompressPriorityComparison</a>
</td>
<td align="left" width="63%">
Sets a priority comparison handler for compression.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setconcludeprioritycomparison">SetConcludePriorityComparison</a>
</td>
<td align="left" width="63%">
Sets a priority comparison handler for conclusion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setdefaultlongestacceptabledelay">SetDefaultLongestAcceptableDelay</a>
</td>
<td align="left" width="63%">
Sets the default acceptable animation delay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setmanagereventhandler">SetManagerEventHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for animation manager status updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-settrimprioritycomparison">SetTrimPriorityComparison</a>
</td>
<td align="left" width="63%">
Sets a priority comparison handler for trimming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the animation manager and all its associated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-update">Update</a>
</td>
<td align="left" width="63%">
Updates the values of all animation variables.

</td>
</tr>
</table> 


## -remarks



<b>IUIAnimationManager</b> defines a central control object for animations.
         
         A single instance of <b>IUIAnimationManager</b> is typically used to compose, schedule, 
         and manage all animations for a client application.


<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>,
         <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>, and 
         <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>are the primary components for building animations.
         
         Use <b>IUIAnimationManager</b> to create and manage these components.


#### Examples

For an example that creates the animation manager object, see <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/adding-animation-to-an-application">Create the Main Animation Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

