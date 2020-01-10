---
UID: NF:uianimation.IUIAnimationStoryboard.GetStatus
title: IUIAnimationStoryboard::GetStatus (uianimation.h)
description: Gets the status of the storyboard.
old-location: uianimation\iuianimationstoryboard_getstatus.htm
tech.root: UIAnimation
ms.assetid: 8ee9a17f-c57c-49df-950d-491e05ba8768
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Windows Animation], GetStatus method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],GetStatus method, IUIAnimationStoryboard.GetStatus, IUIAnimationStoryboard::GetStatus, uianimation.iuianimationstoryboard_getstatus, uianimation/IUIAnimationStoryboard::GetStatus
f1_keywords:
- uianimation/IUIAnimationStoryboard.GetStatus
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAnimation.dll
api_name:
- IUIAnimationStoryboard.GetStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationStoryboard::GetStatus


## -description


Gets the status of the storyboard.


## -parameters




### -param status [out]

The storyboard status.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Unless this method is called from a handler for <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">OnStoryboardStatusChanged</a> events, the only values it returns are <b>UI_ANIMATION_STORYBOARD_BUILDING</b>, <b>UI_ANIMATION_STORYBOARD_SCHEDULED</b>,
<b>UI_ANIMATION_STORYBOARD_PLAYING</b>, and <b>UI_ANIMATION_STORYBOARD_READY</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged</a>



<a href="https://docs.microsoft.com/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

