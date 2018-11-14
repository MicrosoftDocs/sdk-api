---
UID: NF:dinputd.IDirectInputEffectDriver.StartEffect
title: IDirectInputEffectDriver::StartEffect
author: windows-sdk-content
description: The IDirectInputEffectDriver::StartEffect method begins the playback of an effect. If the effect is already playing, it is restarted from the beginning.
old-location: hid\idirectinputeffectdriver_starteffect.htm
tech.root: hid
ms.assetid: 2c1865c2-ded4-47ce-a743-8ac48986dc5f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDirectInputEffectDriver interface [Human Input Devices],StartEffect method, IDirectInputEffectDriver.StartEffect, IDirectInputEffectDriver::StartEffect, StartEffect, StartEffect method [Human Input Devices], StartEffect method [Human Input Devices],IDirectInputEffectDriver interface, di_ref_f30aed74-b4e3-41da-b5c7-f153d6f30b40.xml, dinputd/IDirectInputEffectDriver::StartEffect, hid.idirectinputeffectdriver_starteffect
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirectInputEffectDriver.StartEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dinputd.h
: 
- IDirectInputEffectDriver.StartEffect
: 
---

# IDirectInputEffectDriver::StartEffect


## -description


The <b>IDirectInputEffectDriver::StartEffect</b> method begins the playback of an effect. If the effect is already playing, it is restarted from the beginning. 


## -parameters




### -param arg1

Identifies the external joystick number being addressed 


### -param arg2

Specifies the effect to be played. 


### -param arg3

Specifies how the effect is to affect other effects. Only the mode listed below can be used; all other modes are reserved. For example, the driver never receives the DIES_NODOWNLOAD flag because it is managed by DirectInput and not the driver.  This parameter can be zero, one, or more of the following flags:





#### DIES_SOLO

Indicates that all other effects on the device should be stopped before the specified effect is played. If this flag is omitted, the effect is mixed with existing effects that have already started on the device. 


### -param arg4

Specifies the number of times to perform the effect. If the value is INFINITE, then the effect should be repeated until explicitly stopped or paused. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



