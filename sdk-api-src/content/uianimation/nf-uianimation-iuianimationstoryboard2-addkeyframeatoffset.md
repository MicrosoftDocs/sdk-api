---
UID: NF:uianimation.IUIAnimationStoryboard2.AddKeyframeAtOffset
title: IUIAnimationStoryboard2::AddKeyframeAtOffset (uianimation.h)
author: windows-sdk-content
description: Adds a keyframe at the specified offset from an existing keyframe.
old-location: uianimation\iuianimationstoryboard2_addkeyframeatoffset.htm
tech.root: UIAnimation
ms.assetid: 6AB47BC1-4437-4191-8B66-8545EB4102A9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddKeyframeAtOffset, AddKeyframeAtOffset method [Windows Animation], AddKeyframeAtOffset method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],AddKeyframeAtOffset method, IUIAnimationStoryboard2.AddKeyframeAtOffset, IUIAnimationStoryboard2::AddKeyframeAtOffset, uianimation.iuianimationstoryboard2_addkeyframeatoffset, uianimation/IUIAnimationStoryboard2::AddKeyframeAtOffset
ms.topic: method
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
 - IUIAnimationStoryboard2.AddKeyframeAtOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationStoryboard2::AddKeyframeAtOffset


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



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.




## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/F5D13D36-1AEE-4D47-9683-A428E9ADF1D6">IUIAnimationStoryboard2::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/F4DAB833-E857-4FD8-87E2-8F32AF460F90">IUIAnimationStoryboard2::AddTransitionAtKeyframe</a>



<a href="https://msdn.microsoft.com/55AEA5EA-7D9E-4669-8315-7A6F4428EDF9">IUIAnimationStoryboard2::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/4ac3d524-35a6-4cb9-a468-b7f88500a49c">UI_ANIMATION_KEYFRAME</a>
 

 

