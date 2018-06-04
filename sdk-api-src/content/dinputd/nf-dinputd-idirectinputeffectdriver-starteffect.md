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

# IDirectInputEffectDriver::StartEffect


## -description


The <b>IDirectInputEffectDriver::StartEffect</b> method begins the playback of an effect. If the effect is already playing, it is restarted from the beginning. 


## -parameters




### -param






#### - dwCount

Specifies the number of times to perform the effect. If the value is INFINITE, then the effect should be repeated until explicitly stopped or paused. 


#### - dwEffect

Specifies the effect to be played. 


#### - dwID

Identifies the external joystick number being addressed 


#### - dwMode

Specifies how the effect is to affect other effects. Only the mode listed below can be used; all other modes are reserved. For example, the driver never receives the DIES_NODOWNLOAD flag because it is managed by DirectInput and not the driver.  This parameter can be zero, one, or more of the following flags:





#### DIES_SOLO

Indicates that all other effects on the device should be stopped before the specified effect is played. If this flag is omitted, the effect is mixed with existing effects that have already started on the device. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



