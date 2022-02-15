---
UID: NF:dinputd.IDirectInputEffectDriver.GetForceFeedbackState
title: IDirectInputEffectDriver::GetForceFeedbackState (dinputd.h)
description: The IDirectInputEffectDriver::GetForceFeedbackState method retrieves the force-feedback state for the device.
helpviewer_keywords: ["GetForceFeedbackState","GetForceFeedbackState method [Human Input Devices]","GetForceFeedbackState method [Human Input Devices]","IDirectInputEffectDriver interface","IDirectInputEffectDriver interface [Human Input Devices]","GetForceFeedbackState method","IDirectInputEffectDriver.GetForceFeedbackState","IDirectInputEffectDriver::GetForceFeedbackState","di_ref_a4cecccc-23d2-408c-90af-f178846f3938.xml","dinputd/IDirectInputEffectDriver::GetForceFeedbackState","hid.idirectinputeffectdriver_getforcefeedbackstate"]
old-location: hid\idirectinputeffectdriver_getforcefeedbackstate.htm
tech.root: hid
ms.assetid: 0cf48162-2b43-4417-820b-5197993ac990
ms.date: 12/05/2018
ms.keywords: GetForceFeedbackState, GetForceFeedbackState method [Human Input Devices], GetForceFeedbackState method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],GetForceFeedbackState method, IDirectInputEffectDriver.GetForceFeedbackState, IDirectInputEffectDriver::GetForceFeedbackState, di_ref_a4cecccc-23d2-408c-90af-f178846f3938.xml, dinputd/IDirectInputEffectDriver::GetForceFeedbackState, hid.idirectinputeffectdriver_getforcefeedbackstate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectInputEffectDriver::GetForceFeedbackState
 - dinputd/IDirectInputEffectDriver::GetForceFeedbackState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputEffectDriver.GetForceFeedbackState
---

# IDirectInputEffectDriver::GetForceFeedbackState


## -description

The <b>IDirectInputEffectDriver::GetForceFeedbackState </b> method retrieves the force-feedback state for the device.

## -parameters

### -param unnamedParam1

Indicates the external joystick number being addressed.

### -param unnamedParam2

Points to a <a href="/windows/desktop/api/dinputd/ns-dinputd-didevicestate">DIDEVICESTATE</a> structure that receives the device state. DirectInput sets the <b>dwSize</b> member of the DIDEVICESTATE structure to <b>sizeof</b>(DIDEVICESTATE) before calling this method.

## -returns

Returns S_OK if successful; otherwise, returns an error code.