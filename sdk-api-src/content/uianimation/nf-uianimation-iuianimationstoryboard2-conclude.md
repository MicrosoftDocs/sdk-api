---
UID: NF:uianimation.IUIAnimationStoryboard2.Conclude
title: IUIAnimationStoryboard2::Conclude
author: windows-sdk-content
description: Completes the current iteration of a keyframe loop that is in progress (where the loop is set to UI_ANIMATION_REPEAT_INDEFINITELY), terminates the loop, and continues with the storyboard.
old-location: uianimation\iuianimationstoryboard2_conclude.htm
tech.root: UIAnimation
ms.assetid: C7687E52-433F-4E73-910D-86298E528F7B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Conclude, Conclude method [Windows Animation], Conclude method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],Conclude method, IUIAnimationStoryboard2.Conclude, IUIAnimationStoryboard2::Conclude, uianimation.iuianimationstoryboard2_conclude, uianimation/IUIAnimationStoryboard2::Conclude
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIAnimationStoryboard2.Conclude
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard2::Conclude


## -description


Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a>), terminates the loop, and continues with the storyboard. 


## -parameters






## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method specifies that any subsequent  keyframe loops that have a repetition count of <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) will be skipped while the remainder of the storyboard is played.  

An iteration of a keyframe loop that is in progress will be completed before the remainder of the storyboard plays.

If this method is called at the end of an alternating keyframe loop iteration, the loop is terminated with the  loop value set to the ending loop value.

 If this method is called at the end of a non-alternating keyframe loop iteration, where  "loop wrapping" results in the loop value being set to the starting value of the next iteration, the loop is executed once more in order for the loop value to be set to the ending loop value.

For alternating keyframe loops, each iteration has a starting value that is equivalent to the ending value of the preceding loop. In this case, "loop wrapping" is not an issue.




## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>
 

 

