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

# IDirectInputEffectDriver::SendForceFeedbackCommand


## -description


The <b>IDirectInputEffectDriver::SendForceFeedbackCommand </b>method changes the force-feedback state for the device. 


## -parameters




### -param






#### - dwCommand

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


#### - dwID

Indicates the external joystick number being addressed. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



