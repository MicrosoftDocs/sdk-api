---
UID: NF:uianimation.IUIAnimationManager2.Shutdown
title: IUIAnimationManager2::Shutdown (uianimation.h)
description: Shuts down the animation manager and all its associated objects. (IUIAnimationManager2.Shutdown)
helpviewer_keywords: ["IUIAnimationManager2 interface [Windows Animation]","Shutdown method","IUIAnimationManager2.Shutdown","IUIAnimationManager2::Shutdown","Shutdown","Shutdown method [Windows Animation]","Shutdown method [Windows Animation]","IUIAnimationManager2 interface","uianimation.iuianimationmanager2_shutdown","uianimation/IUIAnimationManager2::Shutdown"]
old-location: uianimation\iuianimationmanager2_shutdown.htm
tech.root: UIAnimation
ms.assetid: F66A987C-E020-4CD6-BE3F-440C3F8B8CF2
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],Shutdown method, IUIAnimationManager2.Shutdown, IUIAnimationManager2::Shutdown, Shutdown, Shutdown method [Windows Animation], Shutdown method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_shutdown, uianimation/IUIAnimationManager2::Shutdown
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
 - IUIAnimationManager2::Shutdown
 - uianimation/IUIAnimationManager2::Shutdown
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
 - IUIAnimationManager2.Shutdown
---

# IUIAnimationManager2::Shutdown


## -description

Shuts down the animation manager and all its associated objects.



## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Calling this method directs the animation manager, and all the objects it created, to 
         release all their pointers to other objects. After <b>IUIAnimationManager2::Shutdown</b> has been called, no other methods may be called on the animation manager or on any objects that it created. An application can call this method to clean up if there is any possibility that the application has introduced a reference cycle that includes some animation objects.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>
