---
UID: NF:uianimation.IUIAnimationStoryboard2.Conclude
title: IUIAnimationStoryboard2::Conclude (uianimation.h)
description: Completes the current iteration of a keyframe loop that is in progress (where the loop is set to UI_ANIMATION_REPEAT_INDEFINITELY), terminates the loop, and continues with the storyboard. (IUIAnimationStoryboard2.Conclude)
helpviewer_keywords: ["Conclude","Conclude method [Windows Animation]","Conclude method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","Conclude method","IUIAnimationStoryboard2.Conclude","IUIAnimationStoryboard2::Conclude","uianimation.iuianimationstoryboard2_conclude","uianimation/IUIAnimationStoryboard2::Conclude"]
old-location: uianimation\iuianimationstoryboard2_conclude.htm
tech.root: UIAnimation
ms.assetid: C7687E52-433F-4E73-910D-86298E528F7B
ms.date: 12/05/2018
ms.keywords: Conclude, Conclude method [Windows Animation], Conclude method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],Conclude method, IUIAnimationStoryboard2.Conclude, IUIAnimationStoryboard2::Conclude, uianimation.iuianimationstoryboard2_conclude, uianimation/IUIAnimationStoryboard2::Conclude
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationStoryboard2::Conclude
 - uianimation/IUIAnimationStoryboard2::Conclude
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationStoryboard2.Conclude
---

# IUIAnimationStoryboard2::Conclude


## -description

Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a>), terminates the loop, and continues with the storyboard.



## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method specifies that any subsequent  keyframe loops that have a repetition count of <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) will be skipped while the remainder of the storyboard is played.  

An iteration of a keyframe loop that is in progress will be completed before the remainder of the storyboard plays.

If this method is called at the end of an alternating keyframe loop iteration, the loop is terminated with the  loop value set to the ending loop value.

 If this method is called at the end of a non-alternating keyframe loop iteration, where  "loop wrapping" results in the loop value being set to the starting value of the next iteration, the loop is executed once more in order for the loop value to be set to the ending loop value.

For alternating keyframe loops, each iteration has a starting value that is equivalent to the ending value of the preceding loop. In this case, "loop wrapping" is not an issue.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>
