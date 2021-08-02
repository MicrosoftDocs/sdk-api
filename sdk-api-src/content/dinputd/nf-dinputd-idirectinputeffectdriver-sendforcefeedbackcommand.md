---
UID: NF:dinputd.IDirectInputEffectDriver.SendForceFeedbackCommand
title: IDirectInputEffectDriver::SendForceFeedbackCommand (dinputd.h)
description: The IDirectInputEffectDriver::SendForceFeedbackCommand method changes the force-feedback state for the device.
helpviewer_keywords: ["IDirectInputEffectDriver interface [Human Input Devices]","SendForceFeedbackCommand method","IDirectInputEffectDriver.SendForceFeedbackCommand","IDirectInputEffectDriver::SendForceFeedbackCommand","SendForceFeedbackCommand","SendForceFeedbackCommand method [Human Input Devices]","SendForceFeedbackCommand method [Human Input Devices]","IDirectInputEffectDriver interface","di_ref_48773665-821d-428e-a637-7dc77a85cd39.xml","dinputd/IDirectInputEffectDriver::SendForceFeedbackCommand","hid.idirectinputeffectdriver_sendforcefeedbackcommand"]
old-location: hid\idirectinputeffectdriver_sendforcefeedbackcommand.htm
tech.root: hid
ms.assetid: 9a872712-32aa-40b6-9d0f-c51d841342cb
ms.date: 12/05/2018
ms.keywords: IDirectInputEffectDriver interface [Human Input Devices],SendForceFeedbackCommand method, IDirectInputEffectDriver.SendForceFeedbackCommand, IDirectInputEffectDriver::SendForceFeedbackCommand, SendForceFeedbackCommand, SendForceFeedbackCommand method [Human Input Devices], SendForceFeedbackCommand method [Human Input Devices],IDirectInputEffectDriver interface, di_ref_48773665-821d-428e-a637-7dc77a85cd39.xml, dinputd/IDirectInputEffectDriver::SendForceFeedbackCommand, hid.idirectinputeffectdriver_sendforcefeedbackcommand
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
 - IDirectInputEffectDriver::SendForceFeedbackCommand
 - dinputd/IDirectInputEffectDriver::SendForceFeedbackCommand
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
 - IDirectInputEffectDriver.SendForceFeedbackCommand
---

# IDirectInputEffectDriver::SendForceFeedbackCommand


## -description

The <b>IDirectInputEffectDriver::SendForceFeedbackCommand </b> method changes the force-feedback state for the device.

## -parameters

### -param unnamedParam1

Indicates the external joystick number being addressed.

### -param unnamedParam2

Indicates which of the following commands is being sent: 





#### DISFFC_RESET

Indicates that playback of any active effects should be stopped and that all effects should be removed from the device. Once the device has been reset, all effects are no longer valid and must be recreated. 



#### DISFFC_STOPALL

Indicates that playback of all effects should be stopped. Sending the DISFFC_STOPALL command is equivalent to invoking the <b>IDirectInputEffect::Stop</b> method on all effects that are playing. If the device is in a paused state, the device driver is permitted to lose the paused state. 



#### DISFFC_PAUSE

Indicates that playback of all effects should be paused. When effects are paused, time "stops" until the DISFFC_CONTINUE command is sent. For example, suppose an effect of five seconds duration is started. After one second, all effects are paused. After two more seconds, all effects are continued. The effect should then play for four additional seconds. While a force-feedback device is paused, starting a new effect or modifying existing ones can cause the paused state to be lost. 



#### DISFFC_CONTINUE

Indicates that playback should be resumed at the point at which it was interrupted for those effects that were paused by a previous DISFFC_PAUSE command. 



#### DISFFC_SETACTUATORSON

Indicates that the device's force-feedback actuators should be enabled. 



#### DISFFC_SETACTUATORSOFF

Indicates that the device's force-feedback actuators should be disabled. If successful, force feedback effects are "muted". Note that time continues to elapse while actuators are off. For example, suppose an effect of five seconds' duration is started. After one second, actuators are turned off. After two more seconds, actuators are turned back on. The effect should then play for two additional seconds.

## -returns

Returns S_OK if successful; otherwise, returns an error code.

