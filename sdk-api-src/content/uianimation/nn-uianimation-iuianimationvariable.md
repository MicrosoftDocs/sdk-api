---
UID: NN:uianimation.IUIAnimationVariable
title: IUIAnimationVariable (uianimation.h)
description: Defines an animation variable, which represents a visual element that can be animated.
helpviewer_keywords: ["IUIAnimationVariable","IUIAnimationVariable interface [Windows Animation]","IUIAnimationVariable interface [Windows Animation]","described","uianimation.iuianimationvariable","uianimation/IUIAnimationVariable"]
old-location: uianimation\iuianimationvariable.htm
tech.root: UIAnimation
ms.assetid: 1632e62d-6e82-4841-8823-f6b60efc4298
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable, IUIAnimationVariable interface [Windows Animation], IUIAnimationVariable interface [Windows Animation],described, uianimation.iuianimationvariable, uianimation/IUIAnimationVariable
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
 - IUIAnimationVariable
 - uianimation/IUIAnimationVariable
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
 - IUIAnimationVariable
---

# IUIAnimationVariable interface


## -description

Defines an animation variable, which represents a visual element that can be animated.

## -inheritance

The <b>IUIAnimationVariable</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationVariable</b> also has these types of members:

## -remarks

Along with 
         <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a> and 
         <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>, <b>IUIAnimationVariable</b> is a primary component for building animations. To create and manage animation variables, use <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-createanimationvariable">IUIAnimationManager::CreateAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getvariablefromtag">IUIAnimationManager::GetVariableFromTag</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-scheduletransition">IUIAnimationManager::ScheduleTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-holdvariable">IUIAnimationStoryboard::HoldVariable</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
