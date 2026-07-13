---
UID: NN:uianimation.IUIAnimationTimerEventHandler
title: IUIAnimationTimerEventHandler (uianimation.h)
description: Defines methods for handling timing events.
helpviewer_keywords: ["IUIAnimationTimerEventHandler","IUIAnimationTimerEventHandler interface [Windows Animation]","IUIAnimationTimerEventHandler interface [Windows Animation]","described","uianimation.iuianimationtimereventhandler","uianimation/IUIAnimationTimerEventHandler"]
old-location: uianimation\iuianimationtimereventhandler.htm
tech.root: UIAnimation
ms.assetid: 7d5c459e-e1f2-470b-8568-e6847acba63a
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerEventHandler, IUIAnimationTimerEventHandler interface [Windows Animation], IUIAnimationTimerEventHandler interface [Windows Animation],described, uianimation.iuianimationtimereventhandler, uianimation/IUIAnimationTimerEventHandler
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
 - IUIAnimationTimerEventHandler
 - uianimation/IUIAnimationTimerEventHandler
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
 - IUIAnimationTimerEventHandler
---

# IUIAnimationTimerEventHandler interface


## -description

Defines methods for handling timing events.

## -inheritance

The <b>IUIAnimationTimerEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTimerEventHandler</b> also has these types of members:

## -remarks

Use 
         <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimereventhandler">SetTimerEventHandler</a> to specify the timing events handler for an instance of
         <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>. 
      


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/updating---application-driven-animation">Read the Animation Variable Values and Draw Frames</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerclienteventhandler">IUIAnimationTimerClientEventHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
