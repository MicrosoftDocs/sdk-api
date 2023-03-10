---
UID: NF:uianimation.IUIAnimationStoryboard2.SetStoryboardEventHandler
title: IUIAnimationStoryboard2::SetStoryboardEventHandler (uianimation.h)
description: Specifies a handler for storyboard events. (IUIAnimationStoryboard2.SetStoryboardEventHandler)
helpviewer_keywords: ["IUIAnimationStoryboard2 interface [Windows Animation]","SetStoryboardEventHandler method","IUIAnimationStoryboard2.SetStoryboardEventHandler","IUIAnimationStoryboard2::SetStoryboardEventHandler","SetStoryboardEventHandler","SetStoryboardEventHandler method [Windows Animation]","SetStoryboardEventHandler method [Windows Animation]","IUIAnimationStoryboard2 interface","uianimation.iuianimationstoryboard2_setstoryboardeventhandler","uianimation/IUIAnimationStoryboard2::SetStoryboardEventHandler"]
old-location: uianimation\iuianimationstoryboard2_setstoryboardeventhandler.htm
tech.root: UIAnimation
ms.assetid: 9C105DDC-4BED-45FC-B4AE-2331A228BB86
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard2 interface [Windows Animation],SetStoryboardEventHandler method, IUIAnimationStoryboard2.SetStoryboardEventHandler, IUIAnimationStoryboard2::SetStoryboardEventHandler, SetStoryboardEventHandler, SetStoryboardEventHandler method [Windows Animation], SetStoryboardEventHandler method [Windows Animation],IUIAnimationStoryboard2 interface, uianimation.iuianimationstoryboard2_setstoryboardeventhandler, uianimation/IUIAnimationStoryboard2::SetStoryboardEventHandler
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
 - IUIAnimationStoryboard2::SetStoryboardEventHandler
 - uianimation/IUIAnimationStoryboard2::SetStoryboardEventHandler
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
 - IUIAnimationStoryboard2.SetStoryboardEventHandler
---

# IUIAnimationStoryboard2::SetStoryboardEventHandler


## -description

Specifies a handler for storyboard events.

## -parameters

### -param handler [in, optional]

The handler that Windows Animation should call whenever storyboard status and update events occur.
            
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboardeventhandler2">IUIAnimationStoryboardEventHandler2</a> interface or be <b>NULL</b>. See Remarks for more info.

### -param fRegisterStatusChangeForNextAnimationEvent [in]

If <b>TRUE</b>, registers the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler2-onstoryboardstatuschanged">OnStoryboardStatusChanged</a> event and includes those events in <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-estimatenexteventtime">IUIAnimationManager2::EstimateNextEventTime</a>, which estimates the time interval until the next animation event. No default value.

### -param fRegisterUpdateForNextAnimationEvent [in]

If <b>TRUE</b>, registers the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler2-onstoryboardupdated">OnStoryboardUpdated</a> event and includes those events in <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-estimatenexteventtime">IUIAnimationManager2::EstimateNextEventTime</a>, which estimates the time interval until the next animation event. No default value.

## -returns

Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-shutdown">IUIAnimationManager2::Shutdown</a> method.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboardeventhandler2">IUIAnimationStoryboardEventHandler2</a>
