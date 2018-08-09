---
UID: NF:dinputd.IDirectInputEffectDriver.GetForceFeedbackState
title: IDirectInputEffectDriver::GetForceFeedbackState
author: windows-sdk-content
description: The IDirectInputEffectDriver::GetForceFeedbackState method retrieves the force-feedback state for the device.
old-location: hid\idirectinputeffectdriver_getforcefeedbackstate.htm
old-project: hid
ms.assetid: 0cf48162-2b43-4417-820b-5197993ac990
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetForceFeedbackState, GetForceFeedbackState method [Human Input Devices], GetForceFeedbackState method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],GetForceFeedbackState method, IDirectInputEffectDriver.GetForceFeedbackState, IDirectInputEffectDriver::GetForceFeedbackState, di_ref_a4cecccc-23d2-408c-90af-f178846f3938.xml, dinputd/IDirectInputEffectDriver::GetForceFeedbackState, hid.idirectinputeffectdriver_getforcefeedbackstate
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
tech.root: 
req.typenames: DIEFFESCAPE, *LPDIEFFESCAPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputEffectDriver.GetForceFeedbackState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



