---
UID: NF:uianimation.IUIAnimationStoryboard.AddTransition
title: IUIAnimationStoryboard::AddTransition (uianimation.h)
description: Adds a transition to the storyboard. (IUIAnimationStoryboard.AddTransition)
helpviewer_keywords: ["AddTransition","AddTransition method [Windows Animation]","AddTransition method [Windows Animation]","IUIAnimationStoryboard interface","IUIAnimationStoryboard interface [Windows Animation]","AddTransition method","IUIAnimationStoryboard.AddTransition","IUIAnimationStoryboard::AddTransition","uianimation.iuianimationstoryboard_addtransition","uianimation/IUIAnimationStoryboard::AddTransition"]
old-location: uianimation\iuianimationstoryboard_addtransition.htm
tech.root: UIAnimation
ms.assetid: c3213e5d-c8f5-406a-bc44-9de7a740b070
ms.date: 12/05/2018
ms.keywords: AddTransition, AddTransition method [Windows Animation], AddTransition method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],AddTransition method, IUIAnimationStoryboard.AddTransition, IUIAnimationStoryboard::AddTransition, uianimation.iuianimationstoryboard_addtransition, uianimation/IUIAnimationStoryboard::AddTransition
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
 - IUIAnimationStoryboard::AddTransition
 - uianimation/IUIAnimationStoryboard::AddTransition
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
 - IUIAnimationStoryboard.AddTransition
---

# IUIAnimationStoryboard::AddTransition


## -description

Adds a transition to the storyboard.

## -parameters

### -param variable [in]

The animation variable for which the transition is to be added.

### -param transition [in]

 
               The transition to be added.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

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
This transition has already been added to a storyboard.

</td>
</tr>
</table>

## -remarks

The <b>AddTransition</b> method applies the specified transition to the specified variable in the storyboard. If this is the first transition applied to this variable in this storyboard, the transition begins at the start of the storyboard. Otherwise, the transition is appended to the transition that was most recently added to the variable.


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/updating---timer-driven-animation">Create a Storyboard and Add Transitions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>
