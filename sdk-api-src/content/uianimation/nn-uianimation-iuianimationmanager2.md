---
UID: NN:uianimation.IUIAnimationManager2
title: IUIAnimationManager2
author: windows-sdk-content
description: Defines an animation manager, which provides a central interface for creating and managing animations in multiple dimensions.
old-location: uianimation\iuianimationmanager2.htm
old-project: UIAnimation
ms.assetid: BD7DAD23-2A7D-4EE7-9BCF-8380F928674D
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationManager2, IUIAnimationManager2 interface [Windows Animation], IUIAnimationManager2 interface [Windows Animation],described, uianimation.iuianimationmanager2, uianimation/IUIAnimationManager2
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationManager2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager2 interface


## -description


Defines an <b>animation manager</b>, which provides a central interface for creating and managing animations in multiple dimensions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationManager2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationManager2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E8DC71C0-CA68-4FD8-81CE-68450BF4EBA7">AbandonAllStoryboards</a>
</td>
<td align="left" width="63%">

      Abandons all active storyboards.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5E963D24-2436-4B8F-8806-69E521EC83AF">CreateAnimationVariable</a>
</td>
<td align="left" width="63%">
Creates a new animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b102f7d7-1a0b-40b5-bcc6-fa82dbcb4156">CreateAnimationVectorVariable</a>
</td>
<td align="left" width="63%">
Creates a new animation variable for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3D66B9DC-15F0-4660-ACF5-FBC801467FD9">CreateStoryboard</a>
</td>
<td align="left" width="63%">
Creates a new storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C2F049B7-287F-4EC2-A737-965E01515056">EstimateNextEventTime</a>
</td>
<td align="left" width="63%">
Retrieves an estimate of  the time interval before the next animation event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/830A5D30-68FF-4226-AC7C-7B1C5F7BA367">FinishAllStoryboards</a>
</td>
<td align="left" width="63%">

      Finishes all active storyboards within the specified time interval.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">

      Gets the status of the animation manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7B11A34-E5FB-40D7-A655-29D28ECF4068">GetStoryboardFromTag</a>
</td>
<td align="left" width="63%">

      Gets the storyboard with the specified tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ED367DB7-91D6-4D2E-BDAB-27FA4340F091">GetVariableFromTag</a>
</td>
<td align="left" width="63%">

      Gets the animation variable with the specified tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">

      Pauses all animations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/943BCFBB-3E16-4CC8-BA9F-06D4C99B1DF0">Resume</a>
</td>
<td align="left" width="63%">

      Resumes all animations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F0F5D099-6290-485F-AD68-101CD57E8656">ScheduleTransition</a>
</td>
<td align="left" width="63%">

      Creates and schedules a single-transition storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BA568B62-7A85-4758-BB04-B4AF617A8443">SetAnimationMode</a>
</td>
<td align="left" width="63%">

      Sets the animation mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55DEC4C2-A6F3-459D-BDCD-3D3819EBF0D2">SetCancelPriorityComparison</a>
</td>
<td align="left" width="63%">

      Sets the priority comparison handler that determines whether  a scheduled storyboard can be canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A754A307-AFFB-4E43-862D-C2FBC85E6C74">SetCompressPriorityComparison</a>
</td>
<td align="left" width="63%">

      Sets the priority comparison handler that determines whether  a scheduled storyboard can be compressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1BDC9094-6020-4640-B959-59CD6CF48751">SetConcludePriorityComparison</a>
</td>
<td align="left" width="63%">

      Sets the priority comparison handler that determines whether  a scheduled storyboard can be concluded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CB00C22B-9837-43AD-9E04-30182B7386E9">SetDefaultLongestAcceptableDelay</a>
</td>
<td align="left" width="63%">

      Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/057CF933-4C6B-4875-82CD-27BB69ED8E4D">SetManagerEventHandler</a>
</td>
<td align="left" width="63%">

      
         Specifies a handler for animation manager status updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/742BCD19-FC1D-46DE-9CBC-716793259947">SetTrimPriorityComparison</a>
</td>
<td align="left" width="63%">

      Sets the priority comparison handler that determines whether  a scheduled storyboard can be trimmed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
</td>
<td align="left" width="63%">

      Shuts down the animation manager and all its associated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Updates the values of all animation variables.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

