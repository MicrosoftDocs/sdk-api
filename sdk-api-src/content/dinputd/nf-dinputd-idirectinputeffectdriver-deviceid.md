---
UID: NF:dinputd.IDirectInputEffectDriver.DeviceID
title: IDirectInputEffectDriver::DeviceID (dinputd.h)
author: windows-sdk-content
description: The IDirectInputEffectDriver::DeviceID method sends the driver the identity of the device.
old-location: hid\idirectinputeffectdriver_deviceid.htm
tech.root: hid
ms.assetid: 80abcfef-edd9-48df-8e47-96731ae41f8a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeviceID, DeviceID method [Human Input Devices], DeviceID method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],DeviceID method, IDirectInputEffectDriver.DeviceID, IDirectInputEffectDriver::DeviceID, di_ref_80f2cc7f-de04-4497-a245-b6abaf0a98d1.xml, dinputd/IDirectInputEffectDriver::DeviceID, hid.idirectinputeffectdriver_deviceid
ms.topic: method
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputEffectDriver.DeviceID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectInputEffectDriver::DeviceID


## -description


The <b>IDirectInputEffectDriver::DeviceID </b>method sends the driver the identity of the device. 


## -parameters




### -param arg1

Specifies the version number of DirectInput that loaded the effect driver. For example, with DirectInput 5.0, the value of this parameter is 0x00000500. 


### -param arg2

Specifies the joystick ID number. The Microsoft Windows joystick subsystem allocates external IDs. 


### -param arg3

Specifies the availability of the device. This value is nonzero if access to the device is beginning, and zero if access to the device is ending. 


### -param arg4

Specifies the ID of the internal joystick. The device driver manages internal IDs. 


### -param arg5

Points to a <a href="https://msdn.microsoft.com/7eaf2d1e-f216-4678-9c8f-e6c38f6e4e66">DIHIDFFINITINFO</a> structure that contains initialization information for the force feedback driver. The driver uses this information to distinguish between multiple devices and to query DirectInput for any other device attributes.


## -returns



Returns S_OK if successful; otherwise, returns an error code.




## -remarks



As an example of the <b>IDirectInputEffectDriver::DeviceID </b>method, if a device driver is passed <i>dwExternalID</i> = 2 and <i>dwInternalId</i> = 1, then unit 1 on the device corresponds to the joystick whose ID is 2.



