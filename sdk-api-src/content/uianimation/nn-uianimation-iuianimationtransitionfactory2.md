---
UID: NN:uianimation.IUIAnimationTransitionFactory2
title: IUIAnimationTransitionFactory2 (uianimation.h)
description: Defines a method for creating transitions from custom interpolators. supports the creation of transitions in a specified dimension.
helpviewer_keywords: ["IUIAnimationTransitionFactory2","IUIAnimationTransitionFactory2 interface [Windows Animation]","IUIAnimationTransitionFactory2 interface [Windows Animation]","described","uianimation.iuianimationtransitionfactory2","uianimation/IUIAnimationTransitionFactory2"]
old-location: uianimation\iuianimationtransitionfactory2.htm
tech.root: UIAnimation
ms.assetid: EB829B6A-770C-486A-9BA2-4D7C8F073C8F
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransitionFactory2, IUIAnimationTransitionFactory2 interface [Windows Animation], IUIAnimationTransitionFactory2 interface [Windows Animation],described, uianimation.iuianimationtransitionfactory2, uianimation/IUIAnimationTransitionFactory2
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
 - IUIAnimationTransitionFactory2
 - uianimation/IUIAnimationTransitionFactory2
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
 - IUIAnimationTransitionFactory2
---

# IUIAnimationTransitionFactory2 interface


## -description

Defines a method for creating transitions from custom interpolators.

<b>IUIAnimationTransitionFactory2</b> supports the creation of transitions in a specified dimension.

## -inheritance

The <b>IUIAnimationTransitionFactory2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTransitionFactory2</b> also has these types of members:

## -remarks

When an application requires animation effects that are not available in the transition library, developers can implement custom transitions that the application can use. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from the interpolator. An interpolator must implement either the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a> interface or the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a> interface; an implementation of the transition factory object is provided by <a href="/previous-versions/windows/desktop/legacy/dd317024(v=vs.85)">UIAnimationTransitionFactory</a> or by <a href="/previous-versions/windows/desktop/legacy/hh448667(v=vs.85)">UIAnimationTransitionFactory2</a>.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>
