---
UID: NF:dinputd.IDirectInputEffectDriver.GetEffectStatus
title: IDirectInputEffectDriver::GetEffectStatus (dinputd.h)
description: The IDirectInputEffectDriver::GetEffectStatus method obtains information about the status of an effect.
helpviewer_keywords: ["GetEffectStatus","GetEffectStatus method [Human Input Devices]","GetEffectStatus method [Human Input Devices]","IDirectInputEffectDriver interface","IDirectInputEffectDriver interface [Human Input Devices]","GetEffectStatus method","IDirectInputEffectDriver.GetEffectStatus","IDirectInputEffectDriver::GetEffectStatus","di_ref_983ce615-4a09-4d28-af9d-968cd6c7054f.xml","dinputd/IDirectInputEffectDriver::GetEffectStatus","hid.idirectinputeffectdriver_geteffectstatus"]
old-location: hid\idirectinputeffectdriver_geteffectstatus.htm
tech.root: hid
ms.assetid: 1332b89a-59ab-4baf-a729-2183b24ce70d
ms.date: 12/05/2018
ms.keywords: GetEffectStatus, GetEffectStatus method [Human Input Devices], GetEffectStatus method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],GetEffectStatus method, IDirectInputEffectDriver.GetEffectStatus, IDirectInputEffectDriver::GetEffectStatus, di_ref_983ce615-4a09-4d28-af9d-968cd6c7054f.xml, dinputd/IDirectInputEffectDriver::GetEffectStatus, hid.idirectinputeffectdriver_geteffectstatus
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
 - IDirectInputEffectDriver::GetEffectStatus
 - dinputd/IDirectInputEffectDriver::GetEffectStatus
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
 - IDirectInputEffectDriver.GetEffectStatus
---

# IDirectInputEffectDriver::GetEffectStatus


## -description

The <b>IDirectInputEffectDriver::GetEffectStatus </b> method obtains information about the status of an effect.

## -parameters

### -param unnamedParam1

Indicates the external joystick number being addressed.

### -param unnamedParam2

Specifies the effect to be queried.

### -param unnamedParam3

Points to a <b>DWORD </b> that receives the effect status. The <b>DWORD</b> should be filled in with one of the following values: 





#### DIEGES_PLAYING

The effect is still playing. 



#### 0

The effect is not playing.

## -returns

Returns S_OK if successful; otherwise, returns an error code.

