---
UID: NN:uianimation.IUIAnimationTimerUpdateHandler
title: IUIAnimationTimerUpdateHandler (uianimation.h)
description: Defines methods for handling timing update events.
helpviewer_keywords: ["IUIAnimationTimerUpdateHandler","IUIAnimationTimerUpdateHandler interface [Windows Animation]","IUIAnimationTimerUpdateHandler interface [Windows Animation]","described","uianimation.iuianimationtimerupdatehandler","uianimation/IUIAnimationTimerUpdateHandler"]
old-location: uianimation\iuianimationtimerupdatehandler.htm
tech.root: UIAnimation
ms.assetid: f155ed12-d493-48a0-9bdf-0e1e79cbcd38
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerUpdateHandler, IUIAnimationTimerUpdateHandler interface [Windows Animation], IUIAnimationTimerUpdateHandler interface [Windows Animation],described, uianimation.iuianimationtimerupdatehandler, uianimation/IUIAnimationTimerUpdateHandler
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
 - IUIAnimationTimerUpdateHandler
 - uianimation/IUIAnimationTimerUpdateHandler
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
 - IUIAnimationTimerUpdateHandler
---

# IUIAnimationTimerUpdateHandler interface


## -description

Defines methods for handling timing update events.

## -inheritance

The <b>IUIAnimationTimerUpdateHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTimerUpdateHandler</b> also has these types of members:

## -remarks

The <a href="/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)">UIAnimationManager</a> object implements this interface, so a client application can query the <b>UIAnimationManager</b> object for this interface and then pass the interface to <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimerupdatehandler">IUIAnimationTimer::SetTimerUpdateHandler</a>.  It is not necessary to disconnect the <b>UIAnimationManager</b> and <a href="/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)">UIAnimationTimer</a> objects; releasing them both is sufficient to clean up.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerclienteventhandler">IUIAnimationTimerClientEventHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
