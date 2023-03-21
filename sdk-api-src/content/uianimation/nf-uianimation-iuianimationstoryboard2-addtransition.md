---
UID: NF:uianimation.IUIAnimationStoryboard2.AddTransition
title: IUIAnimationStoryboard2::AddTransition (uianimation.h)
description: Adds a transition to the storyboard. (IUIAnimationStoryboard2.AddTransition)
helpviewer_keywords: ["AddTransition","AddTransition method [Windows Animation]","AddTransition method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","AddTransition method","IUIAnimationStoryboard2.AddTransition","IUIAnimationStoryboard2::AddTransition","uianimation.iuianimationstoryboard2_addtransition","uianimation/IUIAnimationStoryboard2::AddTransition"]
old-location: uianimation\iuianimationstoryboard2_addtransition.htm
tech.root: UIAnimation
ms.assetid: BFC05D67-EE1C-489E-9A8C-10F0AAB24A0A
ms.date: 12/05/2018
ms.keywords: AddTransition, AddTransition method [Windows Animation], AddTransition method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],AddTransition method, IUIAnimationStoryboard2.AddTransition, IUIAnimationStoryboard2::AddTransition, uianimation.iuianimationstoryboard2_addtransition, uianimation/IUIAnimationStoryboard2::AddTransition
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
 - IUIAnimationStoryboard2::AddTransition
 - uianimation/IUIAnimationStoryboard2::AddTransition
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
 - IUIAnimationStoryboard2.AddTransition
---

# IUIAnimationStoryboard2::AddTransition


## -description

Adds a transition to the storyboard.

## -parameters

### -param variable [in]

The animation variable for which the transition is to be added.

### -param transition [in]

 
               The transition to be added.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code.

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
 

See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The <b>AddTransition</b> method applies the specified transition to the specified variable in the storyboard. If this is the first transition applied to this variable in this storyboard, the transition begins at the start of the storyboard. Otherwise, the transition is appended to the transition that was most recently added to the variable.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeaftertransition">IUIAnimationStoryboard2::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionbetweenkeyframes">IUIAnimationStoryboard2::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>
