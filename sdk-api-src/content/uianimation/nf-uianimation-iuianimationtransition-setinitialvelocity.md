---
UID: NF:uianimation.IUIAnimationTransition.SetInitialVelocity
title: IUIAnimationTransition::SetInitialVelocity (uianimation.h)
description: Sets the initial velocity for the transition.
helpviewer_keywords: ["IUIAnimationTransition interface [Windows Animation]","SetInitialVelocity method","IUIAnimationTransition.SetInitialVelocity","IUIAnimationTransition::SetInitialVelocity","SetInitialVelocity","SetInitialVelocity method [Windows Animation]","SetInitialVelocity method [Windows Animation]","IUIAnimationTransition interface","uianimation.iuianimationtransition_setinitialvelocity","uianimation/IUIAnimationTransition::SetInitialVelocity"]
old-location: uianimation\iuianimationtransition_setinitialvelocity.htm
tech.root: UIAnimation
ms.assetid: adb5a173-6efa-4b1b-8e2f-1d69288653ae
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransition interface [Windows Animation],SetInitialVelocity method, IUIAnimationTransition.SetInitialVelocity, IUIAnimationTransition::SetInitialVelocity, SetInitialVelocity, SetInitialVelocity method [Windows Animation], SetInitialVelocity method [Windows Animation],IUIAnimationTransition interface, uianimation.iuianimationtransition_setinitialvelocity, uianimation/IUIAnimationTransition::SetInitialVelocity
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
 - IUIAnimationTransition::SetInitialVelocity
 - uianimation/IUIAnimationTransition::SetInitialVelocity
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
 - IUIAnimationTransition.SetInitialVelocity
---

# IUIAnimationTransition::SetInitialVelocity


## -description

Sets the initial velocity for the transition.

## -parameters

### -param velocity [in]

The initial velocity for the transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method should not be called after the transition has been added to a storyboard.