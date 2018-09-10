---
UID: NF:uianimation.IUIAnimationStoryboard.AddTransitionAtKeyframe
title: IUIAnimationStoryboard::AddTransitionAtKeyframe
author: windows-sdk-content
description: Adds a transition that starts at the specified keyframe.
old-location: uianimation\iuianimationstoryboard_addtransitionatkeyframe.htm
tech.root: UIAnimation
ms.assetid: 94a9aafc-fe5a-49a8-8e14-9e7c4624869a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddTransitionAtKeyframe, AddTransitionAtKeyframe method [Windows Animation], AddTransitionAtKeyframe method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],AddTransitionAtKeyframe method, IUIAnimationStoryboard.AddTransitionAtKeyframe, IUIAnimationStoryboard::AddTransitionAtKeyframe, uianimation.iuianimationstoryboard_addtransitionatkeyframe, uianimation/IUIAnimationStoryboard::AddTransitionAtKeyframe
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
 - IUIAnimationStoryboard.AddTransitionAtKeyframe
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard::AddTransitionAtKeyframe


## -description


Adds a transition that starts at the specified keyframe.


## -parameters




### -param variable [in]

The animation variable for which a transition is to be added.


### -param transition [in]

The transition to be added.


### -param startKeyframe [in]

The keyframe that specifies the beginning of the new transition.


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
</table>
 




## -remarks



Transitions must be added in the order in which they will be played. A transition may begin playing before the preceding transition in the storyboard has finished, in which case the initial value and velocity seen by the new transition is determined by the state of the preceding one. A transition should not begin before the start of the preceding transition.

A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.




## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/f598c8a4-4325-49ed-bc18-5d672e089592">IUIAnimationStoryboard::AddKeyframeAtOffset</a>



<a href="https://msdn.microsoft.com/c3213e5d-c8f5-406a-bc44-9de7a740b070">IUIAnimationStoryboard::AddTransition</a>



<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

