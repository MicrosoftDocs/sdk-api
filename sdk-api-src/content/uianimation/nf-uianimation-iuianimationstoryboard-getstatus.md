---
UID: NF:uianimation.IUIAnimationStoryboard.GetStatus
title: IUIAnimationStoryboard::GetStatus
author: windows-sdk-content
description: Gets the status of the storyboard.
old-location: uianimation\iuianimationstoryboard_getstatus.htm
tech.root: UIAnimation
ms.assetid: 8ee9a17f-c57c-49df-950d-491e05ba8768
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetStatus, GetStatus method [Windows Animation], GetStatus method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],GetStatus method, IUIAnimationStoryboard.GetStatus, IUIAnimationStoryboard::GetStatus, uianimation.iuianimationstoryboard_getstatus, uianimation/IUIAnimationStoryboard::GetStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationStoryboard.GetStatus
: 
---

# IUIAnimationStoryboard::GetStatus


## -description


Gets the status of the storyboard.


## -parameters




### -param status [out]

The storyboard status.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Unless this method is called from a handler for <a href="https://msdn.microsoft.com/e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd">OnStoryboardStatusChanged</a> events, the only values it returns are <b>UI_ANIMATION_STORYBOARD_BUILDING</b>, <b>UI_ANIMATION_STORYBOARD_SCHEDULED</b>,
<b>UI_ANIMATION_STORYBOARD_PLAYING</b>, and <b>UI_ANIMATION_STORYBOARD_READY</b>.




## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd">IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

