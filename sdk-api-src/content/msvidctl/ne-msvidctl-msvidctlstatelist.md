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

# MSVidCtlStateList enumeration


## -description



This topic applies to Windows XP or later.
        



The <b>MSVidCtlStateList</b> enumeration defines the possible state values of the Video Control or the underlying filter graph.


## -enum-fields




### -field STATE_UNBUILT

Indicates that there is no filter graph.


### -field STATE_STOP

Indicates that the Video Control is stopped.


### -field STATE_PAUSE

Indicates that the Video Control is paused.


### -field STATE_PLAY

Indicates that the Video Control is playing.


## -see-also




<a href="https://msdn.microsoft.com/0f7a5e37-5a0d-415e-aca0-df5f9448b017">IMSVidDeviceEvent::StateChange</a>



<a href="https://msdn.microsoft.com/3c21f2c6-8eff-4fe5-a383-057f3394d9ee">Video Control Enumerations</a>



<a href="https://msdn.microsoft.com/16dca4ab-be3d-493a-892b-8d90a0baf109">_IMSVidCtlEvents::StateChange</a>
 

 

