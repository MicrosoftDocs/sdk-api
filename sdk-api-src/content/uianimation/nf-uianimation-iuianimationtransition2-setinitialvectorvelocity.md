---
UID: NF:uianimation.IUIAnimationTransition2.SetInitialVectorVelocity
title: IUIAnimationTransition2::SetInitialVectorVelocity (uianimation.h)
description: Sets the initial velocity of the transition for each specified dimension in the animation variable.
helpviewer_keywords: ["IUIAnimationTransition2 interface [Windows Animation]","SetInitialVectorVelocity method","IUIAnimationTransition2.SetInitialVectorVelocity","IUIAnimationTransition2::SetInitialVectorVelocity","SetInitialVectorVelocity","SetInitialVectorVelocity method [Windows Animation]","SetInitialVectorVelocity method [Windows Animation]","IUIAnimationTransition2 interface","uianimation.iuianimationtransition2_setinitialvectorvelocity","uianimation/IUIAnimationTransition2::SetInitialVectorVelocity"]
old-location: uianimation\iuianimationtransition2_setinitialvectorvelocity.htm
tech.root: UIAnimation
ms.assetid: 29EFBBE0-E877-4521-B4A7-E1828E0493B9
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransition2 interface [Windows Animation],SetInitialVectorVelocity method, IUIAnimationTransition2.SetInitialVectorVelocity, IUIAnimationTransition2::SetInitialVectorVelocity, SetInitialVectorVelocity, SetInitialVectorVelocity method [Windows Animation], SetInitialVectorVelocity method [Windows Animation],IUIAnimationTransition2 interface, uianimation.iuianimationtransition2_setinitialvectorvelocity, uianimation/IUIAnimationTransition2::SetInitialVectorVelocity
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
 - IUIAnimationTransition2::SetInitialVectorVelocity
 - uianimation/IUIAnimationTransition2::SetInitialVectorVelocity
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
 - IUIAnimationTransition2.SetInitialVectorVelocity
---

# IUIAnimationTransition2::SetInitialVectorVelocity


## -description

Sets the initial velocity of the transition for each specified dimension in the animation variable.

## -parameters

### -param velocity [in]

A vector (of size <i>cDimension</i>) that contains  the initial velocities for the transition.

### -param cDimension [in]

The number of dimensions that require transition velocities. This parameter specifies the number of values listed in <i>velocity</i>.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>