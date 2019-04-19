---
UID: NE:mbnapi.MBN_READY_STATE
title: MBN_READY_STATE (mbnapi.h)
author: windows-sdk-content
description: The MBN_READY_STATE enumerated type contains values that indicate the readiness of a Mobile Broadband device to engage in cellular network traffic operations.
old-location: mbn\mbn_ready_state.htm
tech.root: mbn
ms.assetid: 4f712cdc-ee9c-4ceb-9bc4-8a4fe19d0a37
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MBN_READY_STATE, MBN_READY_STATE enumeration [Microsoft Broadband Networks], MBN_READY_STATE_BAD_SIM, MBN_READY_STATE_DEVICE_BLOCKED, MBN_READY_STATE_DEVICE_LOCKED, MBN_READY_STATE_FAILURE, MBN_READY_STATE_INITIALIZED, MBN_READY_STATE_NOT_ACTIVATED, MBN_READY_STATE_OFF, MBN_READY_STATE_SIM_NOT_INSERTED, mbn.mbn_ready_state, mbnapi/MBN_READY_STATE, mbnapi/MBN_READY_STATE_BAD_SIM, mbnapi/MBN_READY_STATE_DEVICE_BLOCKED, mbnapi/MBN_READY_STATE_DEVICE_LOCKED, mbnapi/MBN_READY_STATE_FAILURE, mbnapi/MBN_READY_STATE_INITIALIZED, mbnapi/MBN_READY_STATE_NOT_ACTIVATED, mbnapi/MBN_READY_STATE_OFF, mbnapi/MBN_READY_STATE_SIM_NOT_INSERTED
ms.topic: enum
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_READY_STATE
product: Windows
targetos: Windows
req.typenames: MBN_READY_STATE
req.redist: 
ms.custom: 19H1
---

# MBN_READY_STATE enumeration


## -description


The <b>MBN_READY_STATE</b> enumerated type contains values that indicate the readiness of a Mobile Broadband device to engage in cellular network traffic operations.

  These values are returned by the <a href="https://msdn.microsoft.com/4236fd9d-292a-4840-b52e-c28c3e6eea10">GetReadyState</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>.  For a device with a SIM card, this is to signal that the SIM has been initialized and is ready for access.


## -enum-fields




### -field MBN_READY_STATE_OFF

The mobile broadband device stack is off.


### -field MBN_READY_STATE_INITIALIZED

The card and stack is powered up and ready to be used for mobile broadband operations.


### -field MBN_READY_STATE_SIM_NOT_INSERTED

The SIM is not inserted.


### -field MBN_READY_STATE_BAD_SIM

The SIM is invalid  (PIN Unblock Key retrials have exceeded the limit).


### -field MBN_READY_STATE_FAILURE

General device failure.


### -field MBN_READY_STATE_NOT_ACTIVATED

The subscription is not activated.


### -field MBN_READY_STATE_DEVICE_LOCKED

The device is locked by a PIN or password which is preventing the device from initializing and registering onto the network.  The calling application can call the <a href="https://msdn.microsoft.com/34378403-cf58-4ada-9eb6-f5dad5f69bc9">GetPinState</a> method of the <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> interface to get the type of PIN needed to be entered to unlock the device.


### -field MBN_READY_STATE_DEVICE_BLOCKED

The device is blocked by a PIN or password which is preventing the device from initializing and registering onto the network.  The calling application should call the <a href="https://msdn.microsoft.com/7e5ec24c-681c-4259-9f6a-949bf40d5b3e">Unblock</a> method of the <a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a> interface to unblock the device.


### -field MBN_READY_STATE_NO_ESIM_PROFILE



