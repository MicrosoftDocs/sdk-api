---
UID: NF:dinputd.IDirectInputEffectDriver.Release
title: IDirectInputEffectDriver::Release (dinputd.h)
description: The IDirectInputEffectDriver::Release method decreases the reference count of the DirectInputEffectDriver object by 1. This method is part of the IUnknown interface inherited by DirectInputEffectDriver.
helpviewer_keywords: ["IDirectInputEffectDriver interface [Human Input Devices]","Release method","IDirectInputEffectDriver.Release","IDirectInputEffectDriver::Release","Release","Release method [Human Input Devices]","Release method [Human Input Devices]","IDirectInputEffectDriver interface","di_ref_1363e951-bfbc-4918-9c35-3178d2670990.xml","dinputd/IDirectInputEffectDriver::Release","hid.idirectinputeffectdriver_release"]
old-location: hid\idirectinputeffectdriver_release.htm
tech.root: hid
ms.assetid: 04f8c7ab-56d4-4173-be84-b24253a231ab
ms.date: 12/05/2018
ms.keywords: IDirectInputEffectDriver interface [Human Input Devices],Release method, IDirectInputEffectDriver.Release, IDirectInputEffectDriver::Release, Release, Release method [Human Input Devices], Release method [Human Input Devices],IDirectInputEffectDriver interface, di_ref_1363e951-bfbc-4918-9c35-3178d2670990.xml, dinputd/IDirectInputEffectDriver::Release, hid.idirectinputeffectdriver_release
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
 - IDirectInputEffectDriver::Release
 - dinputd/IDirectInputEffectDriver::Release
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dinputd.h
api_name:
 - IDirectInputEffectDriver.Release
---

# IDirectInputEffectDriver::Release


## -description

The <b>IDirectInputEffectDriver::Release </b> method decreases the reference count of the DirectInputEffectDriver object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputEffectDriver.



## -returns

Returns the new reference count of the object.

## -remarks

The DirectInputEffectDriver object deallocates itself when its reference count reaches 0. Use the <b>IDirectInputEffectDriver::AddRef</b> method to increase the reference count of the object by 1.

