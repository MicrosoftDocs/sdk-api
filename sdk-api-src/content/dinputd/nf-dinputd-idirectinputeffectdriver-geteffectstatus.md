---
UID: NF:dinputd.IDirectInputEffectDriver.GetEffectStatus
title: IDirectInputEffectDriver::GetEffectStatus
author: windows-driver-content
description: The IDirectInputEffectDriver::GetEffectStatus method obtains information about the status of an effect.
old-location: hid\idirectinputeffectdriver_geteffectstatus.htm
old-project: hid
ms.assetid: 1332b89a-59ab-4baf-a729-2183b24ce70d
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetEffectStatus, GetEffectStatus method [Human Input Devices], GetEffectStatus method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],GetEffectStatus method, IDirectInputEffectDriver.GetEffectStatus, IDirectInputEffectDriver::GetEffectStatus, di_ref_983ce615-4a09-4d28-af9d-968cd6c7054f.xml, dinputd/IDirectInputEffectDriver::GetEffectStatus, hid.idirectinputeffectdriver_geteffectstatus
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
-	IDirectInputEffectDriver.GetEffectStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectInputEffectDriver::GetEffectStatus


## -description


The <b>IDirectInputEffectDriver::GetEffectStatus </b>method obtains information about the status of an effect. 


## -parameters




### -param






#### - dwEffect

Specifies the effect to be queried. 


#### - dwID

Indicates the external joystick number being addressed. 


#### - pdwStatus

Points to a <b>DWORD </b>that receives the effect status. The <b>DWORD</b> should be filled in with one of the following values: 





#### DIEGES_PLAYING

The effect is still playing. 



#### 0

The effect is not playing. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



