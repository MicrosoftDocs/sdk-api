---
UID: NF:uianimation.IUIAnimationStoryboard.RepeatBetweenKeyframes
title: IUIAnimationStoryboard::RepeatBetweenKeyframes
author: windows-sdk-content
description: Creates a loop between two specified keyframes.
old-location: uianimation\iuianimationstoryboard_repeatbetweenkeyframes.htm
old-project: UIAnimation
ms.assetid: 3c1ddb8c-fcbf-4b0c-8725-35dfc15e3c02
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],RepeatBetweenKeyframes method, IUIAnimationStoryboard.RepeatBetweenKeyframes, IUIAnimationStoryboard::RepeatBetweenKeyframes, RepeatBetweenKeyframes, RepeatBetweenKeyframes method [Windows Animation], RepeatBetweenKeyframes method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_repeatbetweenkeyframes, uianimation/IUIAnimationStoryboard::RepeatBetweenKeyframes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IUIAnimationStoryboard.RepeatBetweenKeyframes
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard::RepeatBetweenKeyframes


## -description



      Creates a loop between two specified keyframes.


## -parameters




### -param startKeyframe [in]


                The keyframe at which the loop is to begin.


### -param endKeyframe [in]


               The keyframe at which the loop is to end. It must not be posssible for <i>endKeyframe</i> to occur earlier in the storyboard than <i>startKeyframe</i>.


### -param repetitionCount [in]


               The number of times the loop is to be repeated; this parameter must be 0 or a positive number.
               Use <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) to repeat the loop indefinitely until the storyboard is trimmed or concluded.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_START_KEYFRAME_AFTER_END</b></dt>
</dl>
</td>
<td width="60%">
The start keyframe might occur after the end keyframe.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_END_KEYFRAME_NOT_DETERMINED</b></dt>
</dl>
</td>
<td width="60%">
It might not be possible to determine the end keyframe time when the start keyframe is reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_LOOPS_OVERLAP</b></dt>
</dl>
</td>
<td width="60%">
Two repeated portions of a storyboard might overlap.

</td>
</tr>
</table>
 




## -remarks



This method directs a storyboard to play the interval between the given keyframes repeatedly before playing the remainder of the storyboard. If a finite repetition count is specified, the loop always plays that number of times. If <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) is specified, the loop repeats until the storyboard is concluded, in which case the current iteration of the loop completes and the remainder of the storyboard plays. A storyboard that loops indefinitely also ends if it is truncated.

Nested and overlapping loops are not supported.

A keyframe represents a moment in time within a storyboard and can be used to specify the start or end times of transitions.  Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.




## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">
      IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/f598c8a4-4325-49ed-bc18-5d672e089592">IUIAnimationStoryboard::AddKeyframeAtOffset</a>
 

 

