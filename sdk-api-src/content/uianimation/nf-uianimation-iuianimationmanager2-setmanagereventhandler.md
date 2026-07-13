---
UID: NF:uianimation.IUIAnimationManager2.SetManagerEventHandler
title: IUIAnimationManager2::SetManagerEventHandler (uianimation.h)
description: Specifies a handler for animation manager status updates. (IUIAnimationManager2.SetManagerEventHandler)
helpviewer_keywords: ["IUIAnimationManager2 interface [Windows Animation]","SetManagerEventHandler method","IUIAnimationManager2.SetManagerEventHandler","IUIAnimationManager2::SetManagerEventHandler","SetManagerEventHandler","SetManagerEventHandler method [Windows Animation]","SetManagerEventHandler method [Windows Animation]","IUIAnimationManager2 interface","uianimation.iuianimationmanager2_setmanagereventhandler","uianimation/IUIAnimationManager2::SetManagerEventHandler"]
old-location: uianimation\iuianimationmanager2_setmanagereventhandler.htm
tech.root: UIAnimation
ms.assetid: 057CF933-4C6B-4875-82CD-27BB69ED8E4D
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],SetManagerEventHandler method, IUIAnimationManager2.SetManagerEventHandler, IUIAnimationManager2::SetManagerEventHandler, SetManagerEventHandler, SetManagerEventHandler method [Windows Animation], SetManagerEventHandler method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_setmanagereventhandler, uianimation/IUIAnimationManager2::SetManagerEventHandler
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
 - IUIAnimationManager2::SetManagerEventHandler
 - uianimation/IUIAnimationManager2::SetManagerEventHandler
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
 - IUIAnimationManager2.SetManagerEventHandler
---

# IUIAnimationManager2::SetManagerEventHandler


## -description

Specifies a handler for animation manager status updates.

## -parameters

### -param handler [in, optional]

The event handler to be called when the status of the animation manager changes.  
               
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanagereventhandler">IUIAnimationManagerEventHandler</a> interface or be <b>NULL</b>. See Remarks for more info.

### -param fRegisterForNextAnimationEvent [in]

If <b>TRUE</b>, specifies that <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-estimatenexteventtime">IUIAnimationManager2::EstimateNextEventTime</a> will incorporate <i>handler</i> into its estimate of the time interval until the next animation event. No default value.

## -returns

Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-shutdown">IUIAnimationManager2::Shutdown</a> method.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanagereventhandler">IUIAnimationManagerEventHandler</a>
