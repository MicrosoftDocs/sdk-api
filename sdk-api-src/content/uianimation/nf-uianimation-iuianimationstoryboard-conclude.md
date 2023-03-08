---
UID: NF:uianimation.IUIAnimationStoryboard.Conclude
title: IUIAnimationStoryboard::Conclude (uianimation.h)
description: Completes the current iteration of a keyframe loop that is in progress (where the loop is set to UI_ANIMATION_REPEAT_INDEFINITELY), terminates the loop, and continues with the storyboard. (IUIAnimationStoryboard.Conclude)
helpviewer_keywords: ["Conclude","Conclude method [Windows Animation]","Conclude method [Windows Animation]","IUIAnimationStoryboard interface","IUIAnimationStoryboard interface [Windows Animation]","Conclude method","IUIAnimationStoryboard.Conclude","IUIAnimationStoryboard::Conclude","uianimation.iuianimationstoryboard_conclude","uianimation/IUIAnimationStoryboard::Conclude"]
old-location: uianimation\iuianimationstoryboard_conclude.htm
tech.root: UIAnimation
ms.assetid: 82f915df-c031-41e9-8347-044b37793182
ms.date: 12/05/2018
ms.keywords: Conclude, Conclude method [Windows Animation], Conclude method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],Conclude method, IUIAnimationStoryboard.Conclude, IUIAnimationStoryboard::Conclude, uianimation.iuianimationstoryboard_conclude, uianimation/IUIAnimationStoryboard::Conclude
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationStoryboard::Conclude
 - uianimation/IUIAnimationStoryboard::Conclude
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
 - IUIAnimationStoryboard.Conclude
---

# IUIAnimationStoryboard::Conclude


## -description

Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <b>UI_ANIMATION_REPEAT_INDEFINITELY</b>), terminates the loop, and continues with the storyboard.



## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method specifies that any subsequent  keyframe loops that have a repetition count of <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) will be skipped while the remainder of the storyboard is played.  

An iteration of a keyframe loop that is in progress will be completed before the remainder of the storyboard plays.

If this method is called  at the end  of a keyframe loop iteration, the loop is terminated and the loop value is set to the starting loop value.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-abandon">IUIAnimationStoryboard::Abandon</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-finish">IUIAnimationStoryboard::Finish</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-schedule">IUIAnimationStoryboard::Schedule</a>
