---
UID: NF:uianimation.IUIAnimationManager2.GetStatus
title: IUIAnimationManager2::GetStatus
author: windows-sdk-content
description: Gets the status of the animation manager.
old-location: uianimation\iuianimationmanager2_getstatus.htm
old-project: UIAnimation
ms.assetid: E989CED1-C6B7-4086-944E-924836AA7ECB
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetStatus, GetStatus method [Windows Animation], GetStatus method [Windows Animation],IUIAnimationManager2 interface, IUIAnimationManager2 interface [Windows Animation],GetStatus method, IUIAnimationManager2.GetStatus, IUIAnimationManager2::GetStatus, uianimation.iuianimationmanager2_getstatus, uianimation/IUIAnimationManager2::GetStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationManager2.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager2::GetStatus


## -description



      Gets the status of the animation manager.


## -parameters




### -param status [out]


                The status of the animation manager.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/17f98ff5-f18e-44be-a8bd-bc5a6467fa83">IUIAnimationManagerEventHandler::OnManagerStatusChanged</a>



<a href="https://msdn.microsoft.com/499c74c0-d1e7-4ab4-9c3a-19c2e1abeda8">
      UI_ANIMATION_MANAGER_STATUS</a>
 

 

