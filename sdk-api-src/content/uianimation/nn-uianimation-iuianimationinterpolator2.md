---
UID: NN:uianimation.IUIAnimationInterpolator2
title: IUIAnimationInterpolator2 (uianimation.h)
description: Extends the IUIAnimationInterpolator interface that defines methods for creating a custom interpolator. IUIAnimationInterpolator2 supports interpolation in a given dimension.
helpviewer_keywords: ["IUIAnimationInterpolator2","IUIAnimationInterpolator2 interface [Windows Animation]","IUIAnimationInterpolator2 interface [Windows Animation]","described","uianimation.iuianimationinterpolator2","uianimation/IUIAnimationInterpolator2"]
old-location: uianimation\iuianimationinterpolator2.htm
tech.root: UIAnimation
ms.assetid: EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04
ms.date: 12/05/2018
ms.keywords: IUIAnimationInterpolator2, IUIAnimationInterpolator2 interface [Windows Animation], IUIAnimationInterpolator2 interface [Windows Animation],described, uianimation.iuianimationinterpolator2, uianimation/IUIAnimationInterpolator2
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
 - IUIAnimationInterpolator2
 - uianimation/IUIAnimationInterpolator2
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
 - IUIAnimationInterpolator2
---

# IUIAnimationInterpolator2 interface


## -description

Extends the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a> interface that defines methods for creating a custom interpolator.   <b>IUIAnimationInterpolator2</b> supports interpolation in a given dimension.

## -inheritance

The <b>IUIAnimationInterpolator2</b> interface inherits from <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a>. <b>IUIAnimationInterpolator2</b> also has these types of members:

## -remarks

Client applications can use the transitions provided in  the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a> or<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a> interfaces, or in a library provided by a third party; however, custom transitions can be created by implementing the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a> or  <b>IUIAnimationInterpolator2</b> interfaces.

Before Windows Animation can use your custom interpolator, you must wrap it in an object that implements the  <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a> interface (by calling <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionfactory-createtransition">IUIAnimationTransitionFactory::CreateTransition</a>) or the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a> interface (by calling  <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionfactory2">IUIAnimationTransitionFactory2::CreateTransition</a>)  and passing in the custom  interpolator.  After the interpolator wrapper has been created, client applications interact with your interpolator using the <b>IUIAnimationTransition</b> or <b>IUIAnimationTransition2</b> interfaces.

Custom interpolators can be reused across applications, but it is recommended that they be exposed using factory interfaces that return an  <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a> interface or an <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a> interface.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprimitiveinterpolation">IUIAnimationPrimitiveInterpolation</a>



<a href="/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>
