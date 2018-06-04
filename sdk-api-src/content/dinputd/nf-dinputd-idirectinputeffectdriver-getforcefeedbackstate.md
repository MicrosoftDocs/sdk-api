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

# IDirectInputEffectDriver::GetForceFeedbackState


## -description


The <b>IDirectInputEffectDriver::GetForceFeedbackState </b>method retrieves the force-feedback state for the device. 


## -parameters




### -param






#### - dwID

Indicates the external joystick number being addressed. 


#### - pds

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538432">DIDEVICESTATE</a> structure that receives the device state. DirectInput sets the <b>dwSize</b> member of the DIDEVICESTATE structure to <b>sizeof</b>(DIDEVICESTATE) before calling this method. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



