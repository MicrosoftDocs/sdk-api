---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0000_0002
title: "__MIDL___MIDL_itf_UIAnimation_0000_0000_0002"
author: windows-sdk-content
description: Defines the activity status of an animation manager.
old-location: uianimation\ui_animation_manager_status.htm
old-project: UIAnimation
ms.assetid: 499c74c0-d1e7-4ab4-9c3a-19c2e1abeda8
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: UI_ANIMATION_MANAGER_BUSY, UI_ANIMATION_MANAGER_IDLE, UI_ANIMATION_MANAGER_STATUS, UI_ANIMATION_MANAGER_STATUS enumeration [Windows Animation], __MIDL___MIDL_itf_UIAnimation_0000_0000_0002, uianimation.ui_animation_manager_status, uianimation/UI_ANIMATION_MANAGER_BUSY, uianimation/UI_ANIMATION_MANAGER_IDLE, uianimation/UI_ANIMATION_MANAGER_STATUS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
req.typenames: UI_ANIMATION_MANAGER_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	UIAnimation.h
api_name:
-	UI_ANIMATION_MANAGER_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL___MIDL_itf_UIAnimation_0000_0000_0002 enumeration


## -description



        		Defines the activity status of an animation manager.


## -enum-fields




### -field UI_ANIMATION_MANAGER_IDLE


            The animation manager is idle; no animations are currently playing.


### -field UI_ANIMATION_MANAGER_BUSY


            The animation manager is busy; at least one animation is currently playing or scheduled.


## -see-also




<a href="https://msdn.microsoft.com/838140c3-12ca-4909-a0f8-713b5472e5a9">
               IUIAnimationManager::GetStatus</a>



<a href="https://msdn.microsoft.com/17f98ff5-f18e-44be-a8bd-bc5a6467fa83">
               IUIAnimationManagerEventHandler::OnManagerStatusChanged</a>
 

 

