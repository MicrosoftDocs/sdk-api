---
UID: NF:dinputd.IDirectInputEffectDriver.DeviceID
title: IDirectInputEffectDriver::DeviceID
author: windows-sdk-content
description: The IDirectInputEffectDriver::DeviceID method sends the driver the identity of the device.
old-location: hid\idirectinputeffectdriver_deviceid.htm
old-project: hid
ms.assetid: 80abcfef-edd9-48df-8e47-96731ae41f8a
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: DeviceID, DeviceID method [Human Input Devices], DeviceID method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],DeviceID method, IDirectInputEffectDriver.DeviceID, IDirectInputEffectDriver::DeviceID, di_ref_80f2cc7f-de04-4497-a245-b6abaf0a98d1.xml, dinputd/IDirectInputEffectDriver::DeviceID, hid.idirectinputeffectdriver_deviceid
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DIEFFESCAPE, *LPDIEFFESCAPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dinputd.h
api_name:
-	IDirectInputEffectDriver.DeviceID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



