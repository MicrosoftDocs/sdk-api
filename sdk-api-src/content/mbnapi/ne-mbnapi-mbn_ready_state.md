---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



