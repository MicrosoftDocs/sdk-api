---
UID: NF:uianimation.IUIAnimationStoryboard2.GetStatus
title: IUIAnimationStoryboard2::GetStatus
author: windows-sdk-content
description: Gets the status of the storyboard.
old-location: uianimation\iuianimationstoryboard2_getstatus.htm
tech.root: UIAnimation
ms.assetid: 1694B720-891A-4214-A009-6AA722E5B83D
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetStatus, GetStatus method [Windows Animation], GetStatus method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],GetStatus method, IUIAnimationStoryboard2.GetStatus, IUIAnimationStoryboard2::GetStatus, uianimation.iuianimationstoryboard2_getstatus, uianimation/IUIAnimationStoryboard2::GetStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationStoryboard2.GetStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard2::GetStatus


## -description


Gets the status of the storyboard.


## -parameters




### -param status [out, retval]

The storyboard status.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Unless this method is called from a handler for <a href="https://msdn.microsoft.com/6C428A75-755D-4171-A714-83FC65A9D972">OnStoryboardStatusChanged</a> events, the only values it returns are <a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">UI_ANIMATION_STORYBOARD_BUILDING</a>, <b>UI_ANIMATION_STORYBOARD_SCHEDULED</b>,
<b>UI_ANIMATION_STORYBOARD_PLAYING</b>, and <b>UI_ANIMATION_STORYBOARD_READY</b>.




## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/6C428A75-755D-4171-A714-83FC65A9D972">IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

