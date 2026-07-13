---
UID: NF:uianimation.IUIAnimationStoryboard.SetStoryboardEventHandler
title: IUIAnimationStoryboard::SetStoryboardEventHandler (uianimation.h)
description: Specifies a handler for storyboard events. (IUIAnimationStoryboard.SetStoryboardEventHandler)
helpviewer_keywords: ["IUIAnimationStoryboard interface [Windows Animation]","SetStoryboardEventHandler method","IUIAnimationStoryboard.SetStoryboardEventHandler","IUIAnimationStoryboard::SetStoryboardEventHandler","SetStoryboardEventHandler","SetStoryboardEventHandler method [Windows Animation]","SetStoryboardEventHandler method [Windows Animation]","IUIAnimationStoryboard interface","uianimation.iuianimationstoryboard_setstoryboardeventhandler","uianimation/IUIAnimationStoryboard::SetStoryboardEventHandler"]
old-location: uianimation\iuianimationstoryboard_setstoryboardeventhandler.htm
tech.root: UIAnimation
ms.assetid: 8fbe8e94-8585-4adc-8643-3962aff6a031
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],SetStoryboardEventHandler method, IUIAnimationStoryboard.SetStoryboardEventHandler, IUIAnimationStoryboard::SetStoryboardEventHandler, SetStoryboardEventHandler, SetStoryboardEventHandler method [Windows Animation], SetStoryboardEventHandler method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_setstoryboardeventhandler, uianimation/IUIAnimationStoryboard::SetStoryboardEventHandler
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
 - IUIAnimationStoryboard::SetStoryboardEventHandler
 - uianimation/IUIAnimationStoryboard::SetStoryboardEventHandler
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
 - IUIAnimationStoryboard.SetStoryboardEventHandler
---

# IUIAnimationStoryboard::SetStoryboardEventHandler


## -description

Specifies a handler for storyboard events.

## -parameters

### -param handler [in, optional]

The handler to be called whenever storyboard status and update events occur.
            
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboardeventhandler">IUIAnimationStoryboardEventHandler</a> interface or be <b>NULL</b>. See Remarks.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">IUIAnimationManager::Shutdown</a> method.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboardeventhandler">IUIAnimationStoryboardEventHandler</a>
