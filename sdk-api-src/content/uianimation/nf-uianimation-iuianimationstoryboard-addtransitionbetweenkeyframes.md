---
UID: NF:uianimation.IUIAnimationStoryboard.AddTransitionBetweenKeyframes
title: IUIAnimationStoryboard::AddTransitionBetweenKeyframes
author: windows-sdk-content
description: Adds a transition between two keyframes.
old-location: uianimation\iuianimationstoryboard_addtransitionbetweenkeyframes.htm
tech.root: UIAnimation
ms.assetid: 75db41ef-526b-40aa-a62d-a4262cc8d80e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddTransitionBetweenKeyframes, AddTransitionBetweenKeyframes method [Windows Animation], AddTransitionBetweenKeyframes method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],AddTransitionBetweenKeyframes method, IUIAnimationStoryboard.AddTransitionBetweenKeyframes, IUIAnimationStoryboard::AddTransitionBetweenKeyframes, uianimation.iuianimationstoryboard_addtransitionbetweenkeyframes, uianimation/IUIAnimationStoryboard::AddTransitionBetweenKeyframes
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIAnimationStoryboard.AddTransitionBetweenKeyframes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationStoryboard.AddTransitionBetweenKeyframes
: 
---

# IUIAnimationStoryboard::AddTransitionBetweenKeyframes


## -description


Adds a transition between two keyframes.


## -parameters




### -param variable [in]

The animation variable for which the transition is to be added.


### -param transition [in]

The transition to be added.


### -param startKeyframe [in]

A keyframe that specifies the beginning of the new transition.


### -param endKeyframe [in]

A keyframe that specifies the end of the new transition. It must not be possible for <i>endKeyframe</i> to appear earlier in the storyboard than <i>startKeyframe</i>.


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
<dt><b>UI_E_TRANSITION_ALREADY_USED</b></dt>
</dl>
</td>
<td width="60%">
This transition has already been added to a storyboard or has been added to a storyboard that has finished playing and been released.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_TRANSITION_ECLIPSED</b></dt>
</dl>
</td>
<td width="60%">
The transition might eclipse the beginning of another transition in the storyboard.

</td>
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
</table>
 




## -remarks



This method applies the specified transition to the specified variable in the storyboard, with the transition starting and ending at the specified keyframes.  If the transition was created with a duration parameter specified, that duration is overwritten with the duration of time between the start and end keyframes. Otherwise, Windows Animation speeds up or slows down the transition as necessary.

A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

Transitions must be added in the order in which they will be played. A transition may begin playing before the preceding transition in the storyboard has finished, in which case the initial value and velocity seen by the new transition will be determined by the state of the preceding one. It must not be possible for a transition to begin before the start of the preceding transition.




## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/f598c8a4-4325-49ed-bc18-5d672e089592">IUIAnimationStoryboard::AddKeyframeAtOffset</a>



<a href="https://msdn.microsoft.com/c3213e5d-c8f5-406a-bc44-9de7a740b070">IUIAnimationStoryboard::AddTransition</a>



<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

