---
UID: NN:uianimation.IUIAnimationInterpolator
title: IUIAnimationInterpolator (uianimation.h)
description: Defines methods for creating a custom interpolator.
helpviewer_keywords: ["IUIAnimationInterpolator","IUIAnimationInterpolator interface [Windows Animation]","IUIAnimationInterpolator interface [Windows Animation]","described","uianimation.iuianimationinterpolator","uianimation/IUIAnimationInterpolator"]
old-location: uianimation\iuianimationinterpolator.htm
tech.root: UIAnimation
ms.assetid: 8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc
ms.date: 12/05/2018
ms.keywords: IUIAnimationInterpolator, IUIAnimationInterpolator interface [Windows Animation], IUIAnimationInterpolator interface [Windows Animation],described, uianimation.iuianimationinterpolator, uianimation/IUIAnimationInterpolator
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
 - IUIAnimationInterpolator
 - uianimation/IUIAnimationInterpolator
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
 - IUIAnimationInterpolator
---

# IUIAnimationInterpolator interface


## -description

Defines methods for creating a custom interpolator.

## -inheritance

The <b>IUIAnimationInterpolator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationInterpolator</b> also has these types of members:

## -remarks

Client applications can use the transitions provided in  <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a> or in a library provided by a third party; however, if you need custom behavior, you can create your own transitions by implementing the <b>IUIAnimationInterpolator</b> interface.

Before Windows Animation can use your custom interpolator, you must wrap it in an object that implements  <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a> by calling the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionfactory-createtransition">IUIAnimationTransitionFactory::CreateTransition</a> method and passing in the custom  interpolator.  After the interpolator is wrapped, client applications interact with your interpolator using the <b>IUIAnimationTransition</b> interface.

Custom interpolators can be reused across applications, but it is recommended that they be exposed using factory interfaces that return <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a> interfaces.


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/custom-interpolator-sample">Custom Interpolator Sample</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionfactory">IUIAnimationTransitionFactory</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
