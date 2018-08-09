---
UID: NF:dinputd.IDirectInputEffectDriver.DestroyEffect
title: IDirectInputEffectDriver::DestroyEffect
author: windows-sdk-content
description: The IDirectInputEffectDriver::DestroyEffect method removes an effect from the device. If the effect is playing, the driver should stop it before unloading it.
old-location: hid\idirectinputeffectdriver_destroyeffect.htm
old-project: hid
ms.assetid: beb5847c-a30e-4ab4-b293-359aca851c6c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DestroyEffect, DestroyEffect method [Human Input Devices], DestroyEffect method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],DestroyEffect method, IDirectInputEffectDriver.DestroyEffect, IDirectInputEffectDriver::DestroyEffect, di_ref_2c37442c-093a-4470-9335-46b5cc488df3.xml, dinputd/IDirectInputEffectDriver::DestroyEffect, hid.idirectinputeffectdriver_destroyeffect
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
 - IDirectInputEffectDriver.DestroyEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectInputEffectDriver::DestroyEffect


## -description


The <b>IDirectInputEffectDriver::DestroyEffect </b>method removes an effect from the device. If the effect is playing, the driver should stop it before unloading it. 


## -parameters




### -param






#### - dwID

Specifies the external joystick number being addressed. 


#### - dwEffect

Specifies the effect to be destroyed. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



