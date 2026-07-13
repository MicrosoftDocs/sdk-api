---
UID: NN:uianimation.IUIAnimationTransition
title: IUIAnimationTransition (uianimation.h)
description: Defines a transition, which determines how an animation variable changes over time.
helpviewer_keywords: ["IUIAnimationTransition","IUIAnimationTransition interface [Windows Animation]","IUIAnimationTransition interface [Windows Animation]","described","uianimation.iuianimationtransition","uianimation/IUIAnimationTransition"]
old-location: uianimation\iuianimationtransition.htm
tech.root: UIAnimation
ms.assetid: 99804a2f-82c9-494c-b75d-69e66f1e49ef
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransition, IUIAnimationTransition interface [Windows Animation], IUIAnimationTransition interface [Windows Animation],described, uianimation.iuianimationtransition, uianimation/IUIAnimationTransition
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
 - IUIAnimationTransition
 - uianimation/IUIAnimationTransition
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
 - IUIAnimationTransition
---

# IUIAnimationTransition interface


## -description

Defines a transition, which determines how an animation variable changes over time.

## -inheritance

The <b>IUIAnimationTransition</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTransition</b> also has these types of members:

## -remarks

<b>IUIAnimationTransition</b> is one of the primary interfaces used to add animation to an application,
         along with 
         the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a> and 
         <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a> interfaces.


<a href="/previous-versions/windows/desktop/legacy/dd317028(v=vs.85)">UIAnimationTransitionLibrary</a> implements
         a library of standard transitions.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-scheduletransition">IUIAnimationManager::ScheduleTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframes</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionfactory">IUIAnimationTransitionFactory</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/UIAnimation/storyboard-construction">Storyboard Overview</a>
