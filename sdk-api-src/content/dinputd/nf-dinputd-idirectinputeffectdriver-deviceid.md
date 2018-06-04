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

# IDirectInputEffectDriver::DeviceID


## -description


The <b>IDirectInputEffectDriver::DeviceID </b>method sends the driver the identity of the device. 


## -parameters




### -param






#### - dwDIVer

Specifies the version number of DirectInput that loaded the effect driver. For example, with DirectInput 5.0, the value of this parameter is 0x00000500. 


#### - dwExternalID

Specifies the joystick ID number. The Microsoft Windows joystick subsystem allocates external IDs. 


#### - dwInternalId

Specifies the ID of the internal joystick. The device driver manages internal IDs. 


#### - fBegin

Specifies the availability of the device. This value is nonzero if access to the device is beginning, and zero if access to the device is ending. 


#### - lpDIHIDInitInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538497">DIHIDFFINITINFO</a> structure that contains initialization information for the force feedback driver. The driver uses this information to distinguish between multiple devices and to query DirectInput for any other device attributes.


## -returns



Returns S_OK if successful; otherwise, returns an error code.




## -remarks



As an example of the <b>IDirectInputEffectDriver::DeviceID </b>method, if a device driver is passed <i>dwExternalID</i> = 2 and <i>dwInternalId</i> = 1, then unit 1 on the device corresponds to the joystick whose ID is 2.



