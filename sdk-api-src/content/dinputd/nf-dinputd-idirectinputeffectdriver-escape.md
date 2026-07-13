---
UID: NF:dinputd.IDirectInputEffectDriver.Escape
title: IDirectInputEffectDriver::Escape (dinputd.h)
description: The IDirectInputEffectDriver::Escape method escapes to the driver. This method is called in response to an application invoking the IDirectInputEffect::Escape or IDirectInputDevice::Escape methods.
helpviewer_keywords: ["Escape","Escape method [Human Input Devices]","Escape method [Human Input Devices]","IDirectInputEffectDriver interface","IDirectInputEffectDriver interface [Human Input Devices]","Escape method","IDirectInputEffectDriver.Escape","IDirectInputEffectDriver::Escape","di_ref_14789995-a66d-4f0b-9ac4-de0852996da6.xml","dinputd/IDirectInputEffectDriver::Escape","hid.idirectinputeffectdriver_escape"]
old-location: hid\idirectinputeffectdriver_escape.htm
tech.root: hid
ms.assetid: 23bef39d-0254-4b8e-9059-32665d35b5cf
ms.date: 12/05/2018
ms.keywords: Escape, Escape method [Human Input Devices], Escape method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],Escape method, IDirectInputEffectDriver.Escape, IDirectInputEffectDriver::Escape, di_ref_14789995-a66d-4f0b-9ac4-de0852996da6.xml, dinputd/IDirectInputEffectDriver::Escape, hid.idirectinputeffectdriver_escape
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
 - IDirectInputEffectDriver::Escape
 - dinputd/IDirectInputEffectDriver::Escape
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
 - IDirectInputEffectDriver.Escape
---

# IDirectInputEffectDriver::Escape


## -description

The <b>IDirectInputEffectDriver::Escape </b> method escapes to the driver. This method is called in response to an application invoking the <b>IDirectInputEffect::Escape</b> or <b>IDirectInputDevice::Escape</b> methods.

## -parameters

### -param unnamedParam1

Indicates the joystick ID number being used.

### -param unnamedParam2

Specifies the effect at which the command is directed, or zero if the command is directed at the device itself and not any particular effect.

### -param unnamedParam3

Points to a <a href="/windows/desktop/api/dinput/ns-dinput-dieffescape">DIEFFESCAPE</a> structure that describes the command to be sent. On success, the <b>cbOutBuffer</b> member contains the number of output buffer bytes actually used.

## -returns

Returns S_OK if successful; otherwise, returns an error code.