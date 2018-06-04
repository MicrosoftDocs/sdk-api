---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

