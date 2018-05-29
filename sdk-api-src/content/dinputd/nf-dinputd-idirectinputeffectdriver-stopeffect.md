---
UID: NF:dinputd.IDirectInputEffectDriver.StopEffect
title: IDirectInputEffectDriver::StopEffect
author: windows-sdk-content
description: The IDirectInputEffectDriver::StopEffect method halts the playback of an effect.
old-location: hid\idirectinputeffectdriver_stopeffect.htm
old-project: hid
ms.assetid: 613cb68f-1fa8-4122-a1c9-feabde2dfbc9
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: IDirectInputEffectDriver interface [Human Input Devices],StopEffect method, IDirectInputEffectDriver.StopEffect, IDirectInputEffectDriver::StopEffect, StopEffect, StopEffect method [Human Input Devices], StopEffect method [Human Input Devices],IDirectInputEffectDriver interface, di_ref_8aed81a3-c45d-4b8e-bcfb-2c17e1a708a2.xml, dinputd/IDirectInputEffectDriver::StopEffect, hid.idirectinputeffectdriver_stopeffect
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
-	IDirectInputEffectDriver.StopEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectInputEffectDriver::StopEffect


## -description


The <b>IDirectInputEffectDriver::StopEffect </b>method halts the playback of an effect. 


## -parameters




### -param






#### - dwEffect

Specifies the effect to be stopped. 


#### - dwID

Indicates the external joystick number being addressed. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



