---
UID: NF:dinputd.IDirectInputEffectDriver.SetGain
title: IDirectInputEffectDriver::SetGain (dinputd.h)
description: The IDirectInputEffectDriver::SetGain method sets the overall device gain.
helpviewer_keywords: ["IDirectInputEffectDriver interface [Human Input Devices]","SetGain method","IDirectInputEffectDriver.SetGain","IDirectInputEffectDriver::SetGain","SetGain","SetGain method [Human Input Devices]","SetGain method [Human Input Devices]","IDirectInputEffectDriver interface","di_ref_8a0a1de3-be33-44e2-9abb-f4b0b0d4bad8.xml","dinputd/IDirectInputEffectDriver::SetGain","hid.idirectinputeffectdriver_setgain"]
old-location: hid\idirectinputeffectdriver_setgain.htm
tech.root: hid
ms.assetid: 6d0089b2-6e77-4308-b29c-7cc38595de6e
ms.date: 12/05/2018
ms.keywords: IDirectInputEffectDriver interface [Human Input Devices],SetGain method, IDirectInputEffectDriver.SetGain, IDirectInputEffectDriver::SetGain, SetGain, SetGain method [Human Input Devices], SetGain method [Human Input Devices],IDirectInputEffectDriver interface, di_ref_8a0a1de3-be33-44e2-9abb-f4b0b0d4bad8.xml, dinputd/IDirectInputEffectDriver::SetGain, hid.idirectinputeffectdriver_setgain
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
 - IDirectInputEffectDriver::SetGain
 - dinputd/IDirectInputEffectDriver::SetGain
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
 - IDirectInputEffectDriver.SetGain
---

# IDirectInputEffectDriver::SetGain


## -description

The <b>IDirectInputEffectDriver::SetGain </b> method sets the overall device gain.

## -parameters

### -param unnamedParam1

Indicates the joystick ID number being used.

### -param unnamedParam2

Specifies the new gain value (1 to 10,000).

## -returns

Returns S_OK if successful; otherwise, returns an error code.

