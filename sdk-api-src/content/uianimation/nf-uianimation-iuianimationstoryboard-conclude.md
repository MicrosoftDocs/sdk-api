---
UID: NF:uianimation.IUIAnimationStoryboard.Conclude
title: IUIAnimationStoryboard::Conclude
author: windows-sdk-content
description: Completes the current iteration of a keyframe loop that is in progress (where the loop is set to UI_ANIMATION_REPEAT_INDEFINITELY), terminates the loop, and continues with the storyboard.
old-location: uianimation\iuianimationstoryboard_conclude.htm
tech.root: UIAnimation
ms.assetid: 82f915df-c031-41e9-8347-044b37793182
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Conclude, Conclude method [Windows Animation], Conclude method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],Conclude method, IUIAnimationStoryboard.Conclude, IUIAnimationStoryboard::Conclude, uianimation.iuianimationstoryboard_conclude, uianimation/IUIAnimationStoryboard::Conclude
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
 - IUIAnimationStoryboard.Conclude
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard::Conclude


## -description


Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <b>UI_ANIMATION_REPEAT_INDEFINITELY</b>), terminates the loop, and continues with the storyboard. 


## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method specifies that any subsequent  keyframe loops that have a repetition count of <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) will be skipped while the remainder of the storyboard is played.  

An iteration of a keyframe loop that is in progress will be completed before the remainder of the storyboard plays.

If this method is called  at the end  of a keyframe loop iteration, the loop is terminated and the loop value is set to the starting loop value.




## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/2350dbd0-3a67-4832-94dd-56adce80a387">IUIAnimationStoryboard::Abandon</a>



<a href="https://msdn.microsoft.com/45d0872a-dbcf-4151-a880-80b2c6fb884c">IUIAnimationStoryboard::Finish</a>



<a href="https://msdn.microsoft.com/b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8">IUIAnimationStoryboard::Schedule</a>
 

 

