---
UID: NN:uianimation.IUIAnimationManager
title: IUIAnimationManager (uianimation.h)
description: Defines the animation manager, which provides a central interface for creating and managing animations.
helpviewer_keywords: ["IUIAnimationManager","IUIAnimationManager interface [Windows Animation]","IUIAnimationManager interface [Windows Animation]","described","uianimation.iuianimationmanager","uianimation/IUIAnimationManager"]
old-location: uianimation\iuianimationmanager.htm
tech.root: UIAnimation
ms.assetid: 21f16c65-90aa-4b1f-93bc-8ee0488c6ded
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager, IUIAnimationManager interface [Windows Animation], IUIAnimationManager interface [Windows Animation],described, uianimation.iuianimationmanager, uianimation/IUIAnimationManager
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
 - IUIAnimationManager
 - uianimation/IUIAnimationManager
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
 - IUIAnimationManager
---

# IUIAnimationManager interface


## -description

Defines the animation manager, which provides a central interface for creating and managing animations.

## -inheritance

The <b>IUIAnimationManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationManager</b> also has these types of members:

## -remarks

<b>IUIAnimationManager</b> defines a central control object for animations.
         
A single instance of <b>IUIAnimationManager</b> is typically used to compose, schedule, and manage all animations for a client application.


<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>, <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>, and <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a> are the primary components for building animations.
         
Use <b>IUIAnimationManager</b> to create and manage these components.


#### Examples

For an example that creates the animation manager object, see <a href="/windows/desktop/UIAnimation/adding-animation-to-an-application">Create the Main Animation Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
