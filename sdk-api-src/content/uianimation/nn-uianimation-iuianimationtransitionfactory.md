---
UID: NN:uianimation.IUIAnimationTransitionFactory
title: IUIAnimationTransitionFactory (uianimation.h)
description: Defines a method for creating transitions from custom interpolators.
helpviewer_keywords: ["IUIAnimationTransitionFactory","IUIAnimationTransitionFactory interface [Windows Animation]","IUIAnimationTransitionFactory interface [Windows Animation]","described","uianimation.iuianimationtransitionfactory","uianimation/IUIAnimationTransitionFactory"]
old-location: uianimation\iuianimationtransitionfactory.htm
tech.root: UIAnimation
ms.assetid: 62aec8da-e067-4b61-9465-e07fb5b42b7f
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransitionFactory, IUIAnimationTransitionFactory interface [Windows Animation], IUIAnimationTransitionFactory interface [Windows Animation],described, uianimation.iuianimationtransitionfactory, uianimation/IUIAnimationTransitionFactory
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
 - IUIAnimationTransitionFactory
 - uianimation/IUIAnimationTransitionFactory
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
 - IUIAnimationTransitionFactory
---

# IUIAnimationTransitionFactory interface


## -description

Defines a method for creating transitions from custom interpolators.

## -inheritance

The <b>IUIAnimationTransitionFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTransitionFactory</b> also has these types of members:

## -remarks

When an application requires animation effects that are not available in the transition library, developers can implement custom transitions that it can use. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from the interpolator. An interpolator must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a> interface; an implementation of the transition factory object is provided by <a href="/previous-versions/windows/desktop/legacy/dd317024(v=vs.85)">UIAnimationTransitionFactory</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
