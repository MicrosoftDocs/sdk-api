---
UID: NF:dinputd.IDirectInputEffectDriver.SetGain
title: IDirectInputEffectDriver::SetGain method
author: windows-driver-content
description: The IDirectInputEffectDriver::SetGain method sets the overall device gain.
old-location: hid\idirectinputeffectdriver_setgain.htm
old-project: hid
ms.assetid: 6d0089b2-6e77-4308-b29c-7cc38595de6e
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: IDirectInputEffectDriver, IDirectInputEffectDriver interface [Human Input Devices], SetGain method, IDirectInputEffectDriver::SetGain, SetGain method [Human Input Devices], SetGain method [Human Input Devices], IDirectInputEffectDriver interface, SetGain,IDirectInputEffectDriver.SetGain, di_ref_8a0a1de3-be33-44e2-9abb-f4b0b0d4bad8.xml, dinputd/IDirectInputEffectDriver::SetGain, hid.idirectinputeffectdriver_setgain
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
req.typenames: DIEFFESCAPE, *LPDIEFFESCAPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dinputd.h
api_name:
-	IDirectInputEffectDriver.SetGain
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectInputEffectDriver::SetGain method


## -description


The <b>IDirectInputEffectDriver::SetGain </b>method sets the overall device gain. 


## -parameters




### -param






#### - dwGain

Specifies the new gain value (1 to 10,000). 


#### - dwID

Indicates the joystick ID number being used. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



