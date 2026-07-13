---
UID: NF:uianimation.IUIAnimationManager.CreateStoryboard
title: IUIAnimationManager::CreateStoryboard (uianimation.h)
description: Creates a new storyboard. (IUIAnimationManager.CreateStoryboard)
helpviewer_keywords: ["CreateStoryboard","CreateStoryboard method [Windows Animation]","CreateStoryboard method [Windows Animation]","IUIAnimationManager interface","IUIAnimationManager interface [Windows Animation]","CreateStoryboard method","IUIAnimationManager.CreateStoryboard","IUIAnimationManager::CreateStoryboard","uianimation.iuianimationmanager_createstoryboard","uianimation/IUIAnimationManager::CreateStoryboard"]
old-location: uianimation\iuianimationmanager_createstoryboard.htm
tech.root: UIAnimation
ms.assetid: 933ffb62-0f69-4225-873b-e2e023939bea
ms.date: 12/05/2018
ms.keywords: CreateStoryboard, CreateStoryboard method [Windows Animation], CreateStoryboard method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],CreateStoryboard method, IUIAnimationManager.CreateStoryboard, IUIAnimationManager::CreateStoryboard, uianimation.iuianimationmanager_createstoryboard, uianimation/IUIAnimationManager::CreateStoryboard
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
 - IUIAnimationManager::CreateStoryboard
 - uianimation/IUIAnimationManager::CreateStoryboard
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
 - IUIAnimationManager.CreateStoryboard
---

# IUIAnimationManager::CreateStoryboard


## -description

Creates a new storyboard.

## -parameters

### -param storyboard [out]

The new storyboard.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Storyboards can specify complex coordinated updates to many animation variables. These updates happen in sequence or in parallel, and they are guaranteed to remain synchronized within the storyboard. A storyboard is created, populated with transitions on animation variables, and then scheduled. 


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/updating---timer-driven-animation">Create a Storyboard and Add Transitions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>
