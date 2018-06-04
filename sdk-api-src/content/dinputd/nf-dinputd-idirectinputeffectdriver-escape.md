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

# IDirectInputEffectDriver::Escape


## -description


The <b>IDirectInputEffectDriver::Escape </b>method escapes to the driver. This method is called in response to an application invoking the <b>IDirectInputEffect::Escape</b> or <b>IDirectInputDevice::Escape</b> methods. 


## -parameters




### -param






#### - dwEffect

Specifies the effect at which the command is directed, or zero if the command is directed at the device itself and not any particular effect. 


#### - dwID

Indicates the joystick ID number being used. 


#### - pesc

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538462">DIEFFESCAPE</a> structure that describes the command to be sent. On success, the <b>cbOutBuffer</b> member contains the number of output buffer bytes actually used. 


## -returns



Returns S_OK if successful; otherwise, returns an error code. 



