---
UID: NF:uianimation.IUIAnimationTransition.IsDurationKnown
title: IUIAnimationTransition::IsDurationKnown (uianimation.h)
description: Determines whether a transition's duration is currently known.
helpviewer_keywords: ["IUIAnimationTransition interface [Windows Animation]","IsDurationKnown method","IUIAnimationTransition.IsDurationKnown","IUIAnimationTransition::IsDurationKnown","IsDurationKnown","IsDurationKnown method [Windows Animation]","IsDurationKnown method [Windows Animation]","IUIAnimationTransition interface","uianimation.iuianimationtransition_isdurationknown","uianimation/IUIAnimationTransition::IsDurationKnown"]
old-location: uianimation\iuianimationtransition_isdurationknown.htm
tech.root: UIAnimation
ms.assetid: 5cb22573-a318-4682-bc82-0a81c9dbdcbe
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransition interface [Windows Animation],IsDurationKnown method, IUIAnimationTransition.IsDurationKnown, IUIAnimationTransition::IsDurationKnown, IsDurationKnown, IsDurationKnown method [Windows Animation], IsDurationKnown method [Windows Animation],IUIAnimationTransition interface, uianimation.iuianimationtransition_isdurationknown, uianimation/IUIAnimationTransition::IsDurationKnown
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
 - IUIAnimationTransition::IsDurationKnown
 - uianimation/IUIAnimationTransition::IsDurationKnown
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
 - IUIAnimationTransition.IsDurationKnown
---

# IUIAnimationTransition::IsDurationKnown


## -description

Determines whether a transition's duration is currently known.



## -returns

Returns S_OK if the duration is known, S_FALSE if the duration is not known, or an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_STORYBOARD_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The storyboard for this transition is currently in schedule.

</td>
</tr>
</table>

## -remarks

This method should not be called when the storyboard to which the transition has been added is scheduled or playing.


#### Examples

For an example, see <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition-getduration">IUIAnimationTransition::GetDuration</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition-getduration">IUIAnimationTransition::GetDuration</a>
