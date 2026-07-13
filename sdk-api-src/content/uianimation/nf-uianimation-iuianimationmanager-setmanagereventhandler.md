---
UID: NF:uianimation.IUIAnimationManager.SetManagerEventHandler
title: IUIAnimationManager::SetManagerEventHandler (uianimation.h)
description: Specifies a handler for animation manager status updates. (IUIAnimationManager.SetManagerEventHandler)
helpviewer_keywords: ["IUIAnimationManager interface [Windows Animation]","SetManagerEventHandler method","IUIAnimationManager.SetManagerEventHandler","IUIAnimationManager::SetManagerEventHandler","SetManagerEventHandler","SetManagerEventHandler method [Windows Animation]","SetManagerEventHandler method [Windows Animation]","IUIAnimationManager interface","uianimation.iuianimationmanager_setmanagereventhandler","uianimation/IUIAnimationManager::SetManagerEventHandler"]
old-location: uianimation\iuianimationmanager_setmanagereventhandler.htm
tech.root: UIAnimation
ms.assetid: 89c4df40-6faa-4b7c-a255-289d1f8a6254
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],SetManagerEventHandler method, IUIAnimationManager.SetManagerEventHandler, IUIAnimationManager::SetManagerEventHandler, SetManagerEventHandler, SetManagerEventHandler method [Windows Animation], SetManagerEventHandler method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_setmanagereventhandler, uianimation/IUIAnimationManager::SetManagerEventHandler
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
 - IUIAnimationManager::SetManagerEventHandler
 - uianimation/IUIAnimationManager::SetManagerEventHandler
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
 - IUIAnimationManager.SetManagerEventHandler
---

# IUIAnimationManager::SetManagerEventHandler


## -description

Specifies a handler for animation manager status updates.

## -parameters

### -param handler [in, optional]

The event handler to be called when the status of the animation manager changes.  
               
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanagereventhandler">IUIAnimationManagerEventHandler</a> interface or be <b>NULL</b>.

See Remarks section for more information.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">IUIAnimationManager::Shutdown</a> method.


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/introducing-windows-animation-manager">Update the Animation Manager and Draw Frames</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanagereventhandler">IUIAnimationManagerEventHandler</a>
