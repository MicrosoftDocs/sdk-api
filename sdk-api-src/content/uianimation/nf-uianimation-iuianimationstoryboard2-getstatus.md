---
UID: NF:uianimation.IUIAnimationStoryboard2.GetStatus
title: IUIAnimationStoryboard2::GetStatus (uianimation.h)
description: Gets the status of the storyboard. (IUIAnimationStoryboard2.GetStatus)
helpviewer_keywords: ["GetStatus","GetStatus method [Windows Animation]","GetStatus method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","GetStatus method","IUIAnimationStoryboard2.GetStatus","IUIAnimationStoryboard2::GetStatus","uianimation.iuianimationstoryboard2_getstatus","uianimation/IUIAnimationStoryboard2::GetStatus"]
old-location: uianimation\iuianimationstoryboard2_getstatus.htm
tech.root: UIAnimation
ms.assetid: 1694B720-891A-4214-A009-6AA722E5B83D
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Windows Animation], GetStatus method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],GetStatus method, IUIAnimationStoryboard2.GetStatus, IUIAnimationStoryboard2::GetStatus, uianimation.iuianimationstoryboard2_getstatus, uianimation/IUIAnimationStoryboard2::GetStatus
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
 - IUIAnimationStoryboard2::GetStatus
 - uianimation/IUIAnimationStoryboard2::GetStatus
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
 - IUIAnimationStoryboard2.GetStatus
---

# IUIAnimationStoryboard2::GetStatus


## -description

Gets the status of the storyboard.

## -parameters

### -param status [out, retval]

The storyboard status.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Unless this method is called from a handler for <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler2-onstoryboardstatuschanged">OnStoryboardStatusChanged</a> events, the only values it returns are <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_BUILDING</a>, <b>UI_ANIMATION_STORYBOARD_SCHEDULED</b>,
<b>UI_ANIMATION_STORYBOARD_PLAYING</b>, and <b>UI_ANIMATION_STORYBOARD_READY</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler2-onstoryboardstatuschanged">IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
