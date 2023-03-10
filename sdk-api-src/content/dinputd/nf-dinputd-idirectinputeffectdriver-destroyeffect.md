---
UID: NF:dinputd.IDirectInputEffectDriver.DestroyEffect
title: IDirectInputEffectDriver::DestroyEffect (dinputd.h)
description: The IDirectInputEffectDriver::DestroyEffect method removes an effect from the device. If the effect is playing, the driver should stop it before unloading it.
helpviewer_keywords: ["DestroyEffect","DestroyEffect method [Human Input Devices]","DestroyEffect method [Human Input Devices]","IDirectInputEffectDriver interface","IDirectInputEffectDriver interface [Human Input Devices]","DestroyEffect method","IDirectInputEffectDriver.DestroyEffect","IDirectInputEffectDriver::DestroyEffect","di_ref_2c37442c-093a-4470-9335-46b5cc488df3.xml","dinputd/IDirectInputEffectDriver::DestroyEffect","hid.idirectinputeffectdriver_destroyeffect"]
old-location: hid\idirectinputeffectdriver_destroyeffect.htm
tech.root: hid
ms.assetid: beb5847c-a30e-4ab4-b293-359aca851c6c
ms.date: 12/05/2018
ms.keywords: DestroyEffect, DestroyEffect method [Human Input Devices], DestroyEffect method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],DestroyEffect method, IDirectInputEffectDriver.DestroyEffect, IDirectInputEffectDriver::DestroyEffect, di_ref_2c37442c-093a-4470-9335-46b5cc488df3.xml, dinputd/IDirectInputEffectDriver::DestroyEffect, hid.idirectinputeffectdriver_destroyeffect
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
 - IDirectInputEffectDriver::DestroyEffect
 - dinputd/IDirectInputEffectDriver::DestroyEffect
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
 - IDirectInputEffectDriver.DestroyEffect
---

# IDirectInputEffectDriver::DestroyEffect


## -description

The <b>IDirectInputEffectDriver::DestroyEffect </b> method removes an effect from the device. If the effect is playing, the driver should stop it before unloading it.

## -parameters

### -param unnamedParam1

Specifies the external joystick number being addressed.

### -param unnamedParam2

Specifies the effect to be destroyed.

## -returns

Returns S_OK if successful; otherwise, returns an error code.

