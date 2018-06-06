---
UID: NF:uianimation.IUIAnimationStoryboard.AddKeyframeAfterTransition
title: IUIAnimationStoryboard::AddKeyframeAfterTransition
author: windows-sdk-content
description: Adds a keyframe at the end of the specified transition.
old-location: uianimation\iuianimationstoryboard_addkeyframeaftertransition.htm
old-project: UIAnimation
ms.assetid: 055206d8-ea9e-4013-89ee-2929bfeb2731
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: AddKeyframeAfterTransition, AddKeyframeAfterTransition method [Windows Animation], AddKeyframeAfterTransition method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],AddKeyframeAfterTransition method, IUIAnimationStoryboard.AddKeyframeAfterTransition, IUIAnimationStoryboard::AddKeyframeAfterTransition, uianimation.iuianimationstoryboard_addkeyframeaftertransition, uianimation/IUIAnimationStoryboard::AddKeyframeAfterTransition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
 - IUIAnimationStoryboard.AddKeyframeAfterTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard::AddKeyframeAfterTransition


## -description



   Adds a keyframe at the end of the specified transition.


## -parameters




### -param transition [in]


            The transition after which a keyframe is to be added.


### -param keyframe [out]


            The keyframe to be added.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e"> Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_TRANSITION_NOT_IN_STORYBOARD</b></dt>
</dl>
</td>
<td width="60%">
The transition has not been added to the storyboard.

</td>
</tr>
</table>
 




## -remarks




         A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.




## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/f598c8a4-4325-49ed-bc18-5d672e089592">
      IUIAnimationStoryboard::AddKeyframeAtOffset</a>



<a href="https://msdn.microsoft.com/c3213e5d-c8f5-406a-bc44-9de7a740b070">IUIAnimationStoryboard::AddTransition</a>



<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">
      IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">
      IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">
      IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">
      IUIAnimationTransitionLibrary</a>



<a href="https://msdn.microsoft.com/4ac3d524-35a6-4cb9-a468-b7f88500a49c">UI_ANIMATION_KEYFRAME</a>
 

 

