---
UID: NF:uianimation.IUIAnimationStoryboard.AddKeyframeAtOffset
title: IUIAnimationStoryboard::AddKeyframeAtOffset
author: windows-sdk-content
description: Adds a keyframe at the specified offset from an existing keyframe.
old-location: uianimation\iuianimationstoryboard_addkeyframeatoffset.htm
old-project: UIAnimation
ms.assetid: f598c8a4-4325-49ed-bc18-5d672e089592
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: AddKeyframeAtOffset, AddKeyframeAtOffset method [Windows Animation], AddKeyframeAtOffset method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],AddKeyframeAtOffset method, IUIAnimationStoryboard.AddKeyframeAtOffset, IUIAnimationStoryboard::AddKeyframeAtOffset, uianimation.iuianimationstoryboard_addkeyframeatoffset, uianimation/IUIAnimationStoryboard::AddKeyframeAtOffset
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
 - IUIAnimationStoryboard.AddKeyframeAtOffset
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard::AddKeyframeAtOffset


## -description



      Adds a keyframe at the specified offset from an existing keyframe.


## -parameters




### -param existingKeyframe [in]


            The existing keyframe. To add a keyframe at an offset from the start of the storyboard, use the special keyframe <a href="https://msdn.microsoft.com/a77a460c-cf19-48a6-838f-c174950308d8">UI_ANIMATION_KEYFRAME_STORYBOARD_START</a>.


### -param offset [in]


            The offset from the existing keyframe at which a new keyframe is to be added.


### -param keyframe [out]


            The keyframe to be added.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.


#### Examples

The following code adds a keyframe at a fixed offset of 0.3 seconds from the keyframe at the start of the storyboard.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>const UI_ANIMATION_SECONDS offset = 0.3;

UI_ANIMATION_KEYFRAME keyframe1;
hr = pStoryboard-&gt;AddKeyframeAtOffset(
       UI_ANIMATION_KEYFRAME_STORYBOARD_START,
       offset,
       &amp;keyframe1
);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">
      IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">
      IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">
      IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/4ac3d524-35a6-4cb9-a468-b7f88500a49c">UI_ANIMATION_KEYFRAME</a>
 

 

