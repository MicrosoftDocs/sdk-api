---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_UIAnimation_0000_0002_0003 structure


## -description


Defines a keyframe, which represents a time offset within a storyboard.


## -struct-fields


## -remarks



This structure should be treated as a handle. It is returned as an output parameter by some methods and should be used only as a  parameter passed back to other methods as an input parameter.


<a href="https://msdn.microsoft.com/a77a460c-cf19-48a6-838f-c174950308d8">UI_ANIMATION_KEYFRAME_STORYBOARD_START</a> represents the implicit keyframe at the start of every storyboard.




## -see-also




<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/f598c8a4-4325-49ed-bc18-5d672e089592">IUIAnimationStoryboard::AddKeyframeAtOffset</a>



<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/3c1ddb8c-fcbf-4b0c-8725-35dfc15e3c02">IUIAnimationStoryboard::RepeatBetweenKeyframes</a>
 

 

