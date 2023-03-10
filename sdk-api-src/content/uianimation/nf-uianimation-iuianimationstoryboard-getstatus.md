---
UID: NF:uianimation.IUIAnimationStoryboard.GetStatus
title: IUIAnimationStoryboard::GetStatus (uianimation.h)
description: Gets the status of the storyboard. (IUIAnimationStoryboard.GetStatus)
helpviewer_keywords: ["GetStatus","GetStatus method [Windows Animation]","GetStatus method [Windows Animation]","IUIAnimationStoryboard interface","IUIAnimationStoryboard interface [Windows Animation]","GetStatus method","IUIAnimationStoryboard.GetStatus","IUIAnimationStoryboard::GetStatus","uianimation.iuianimationstoryboard_getstatus","uianimation/IUIAnimationStoryboard::GetStatus"]
old-location: uianimation\iuianimationstoryboard_getstatus.htm
tech.root: UIAnimation
ms.assetid: 8ee9a17f-c57c-49df-950d-491e05ba8768
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Windows Animation], GetStatus method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],GetStatus method, IUIAnimationStoryboard.GetStatus, IUIAnimationStoryboard::GetStatus, uianimation.iuianimationstoryboard_getstatus, uianimation/IUIAnimationStoryboard::GetStatus
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
 - IUIAnimationStoryboard::GetStatus
 - uianimation/IUIAnimationStoryboard::GetStatus
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
 - IUIAnimationStoryboard.GetStatus
---

# IUIAnimationStoryboard::GetStatus


## -description

Gets the status of the storyboard.

## -parameters

### -param status [out]

The storyboard status.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Unless this method is called from a handler for <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">OnStoryboardStatusChanged</a> events, the only values it returns are <b>UI_ANIMATION_STORYBOARD_BUILDING</b>, <b>UI_ANIMATION_STORYBOARD_SCHEDULED</b>,
<b>UI_ANIMATION_STORYBOARD_PLAYING</b>, and <b>UI_ANIMATION_STORYBOARD_READY</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
