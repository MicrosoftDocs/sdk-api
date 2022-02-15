---
UID: NF:dinputd.IDirectInputEffectDriver.AddRef
title: IDirectInputEffectDriver::AddRef (dinputd.h)
description: The IDirectInputEffectDriver::AddRef method increases the reference count of the DirectInputEffectDriver object by 1. This method is part of the IUnknown interface inherited by DirectInputEffectDriver.
helpviewer_keywords: ["AddRef","AddRef method [Human Input Devices]","AddRef method [Human Input Devices]","IDirectInputEffectDriver interface","IDirectInputEffectDriver interface [Human Input Devices]","AddRef method","IDirectInputEffectDriver.AddRef","IDirectInputEffectDriver::AddRef","di_ref_9a9eb400-fa33-4643-b060-b047bd6e5818.xml","dinputd/IDirectInputEffectDriver::AddRef","hid.idirectinputeffectdriver_addref"]
old-location: hid\idirectinputeffectdriver_addref.htm
tech.root: hid
ms.assetid: 6bdeb92c-09de-4d26-b2ed-9bacb7233886
ms.date: 12/05/2018
ms.keywords: AddRef, AddRef method [Human Input Devices], AddRef method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],AddRef method, IDirectInputEffectDriver.AddRef, IDirectInputEffectDriver::AddRef, di_ref_9a9eb400-fa33-4643-b060-b047bd6e5818.xml, dinputd/IDirectInputEffectDriver::AddRef, hid.idirectinputeffectdriver_addref
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
 - IDirectInputEffectDriver::AddRef
 - dinputd/IDirectInputEffectDriver::AddRef
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
 - IDirectInputEffectDriver.AddRef
---

# IDirectInputEffectDriver::AddRef


## -description

The <b>IDirectInputEffectDriver::AddRef </b> method increases the reference count of the DirectInputEffectDriver object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputEffectDriver.



## -returns

Returns S_OK if successful; otherwise, returns an error code.

## -remarks

When the DirectInputEffectDriver object is created, its reference count should be set to 1. Each time an application obtains an interface to the object or calls the <b>AddRef</b> method, the object's reference count is increased by 1. The application uses the <b>Release</b> method to decrease the reference count of the object by 1.

