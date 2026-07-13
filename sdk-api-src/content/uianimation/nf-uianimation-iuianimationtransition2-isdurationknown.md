---
UID: NF:uianimation.IUIAnimationTransition2.IsDurationKnown
title: IUIAnimationTransition2::IsDurationKnown (uianimation.h)
description: Determines whether the duration of a transition is known.
helpviewer_keywords: ["IUIAnimationTransition2 interface [Windows Animation]","IsDurationKnown method","IUIAnimationTransition2.IsDurationKnown","IUIAnimationTransition2::IsDurationKnown","IsDurationKnown","IsDurationKnown method [Windows Animation]","IsDurationKnown method [Windows Animation]","IUIAnimationTransition2 interface","uianimation.iuianimationtransition2_isdurationknown","uianimation/IUIAnimationTransition2::IsDurationKnown"]
old-location: uianimation\iuianimationtransition2_isdurationknown.htm
tech.root: UIAnimation
ms.assetid: A73065A7-B191-4CB9-A75A-827CFC040C92
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransition2 interface [Windows Animation],IsDurationKnown method, IUIAnimationTransition2.IsDurationKnown, IUIAnimationTransition2::IsDurationKnown, IsDurationKnown, IsDurationKnown method [Windows Animation], IsDurationKnown method [Windows Animation],IUIAnimationTransition2 interface, uianimation.iuianimationtransition2_isdurationknown, uianimation/IUIAnimationTransition2::IsDurationKnown
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
 - IUIAnimationTransition2::IsDurationKnown
 - uianimation/IUIAnimationTransition2::IsDurationKnown
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
 - IUIAnimationTransition2.IsDurationKnown
---

# IUIAnimationTransition2::IsDurationKnown


## -description

Determines whether the duration of a transition is known.



## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method should not be called when the storyboard to which the transition has been added is scheduled or playing.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-getduration">IUIAnimationTransition2::GetDuration</a>
