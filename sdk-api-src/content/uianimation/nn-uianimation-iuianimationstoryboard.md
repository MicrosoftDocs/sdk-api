---
UID: NN:uianimation.IUIAnimationStoryboard
title: IUIAnimationStoryboard (uianimation.h)
description: Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.
helpviewer_keywords: ["IUIAnimationStoryboard","IUIAnimationStoryboard interface [Windows Animation]","IUIAnimationStoryboard interface [Windows Animation]","described","uianimation.iuianimationstoryboard","uianimation/IUIAnimationStoryboard"]
old-location: uianimation\iuianimationstoryboard.htm
tech.root: UIAnimation
ms.assetid: 6b30b660-dfa4-410f-a8de-58ea5c9a104d
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard, IUIAnimationStoryboard interface [Windows Animation], IUIAnimationStoryboard interface [Windows Animation],described, uianimation.iuianimationstoryboard, uianimation/IUIAnimationStoryboard
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
 - IUIAnimationStoryboard
 - uianimation/IUIAnimationStoryboard
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
 - IUIAnimationStoryboard
---

# IUIAnimationStoryboard interface


## -description

Defines a storyboard, which contains a group of transitions
      that are synchronized relative to one another.

## -inheritance

The <b>IUIAnimationStoryboard</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationStoryboard</b> also has these types of members:

## -remarks

<b>IUIAnimationStoryboard</b> is a primary component for building animations,
         along with 
         <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a> and 
         <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-abandonallstoryboards">IUIAnimationManager::AbandonAllStoryboards</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-createstoryboard">IUIAnimationManager::CreateStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-finishallstoryboards">IUIAnimationManager::FinishAllStoryboards</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstoryboardfromtag">IUIAnimationManager::GetStoryboardFromTag</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getcurrentstoryboard">IUIAnimationVariable::GetCurrentStoryboard</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/UIAnimation/storyboard-construction">Storyboard Overview</a>
