---
UID: NC:bthledef.PFNBLUETOOTH_GATT_EVENT_CALLBACK
title: PFNBLUETOOTH_GATT_EVENT_CALLBACK
author: windows-sdk-content
description: Profile drivers implement a Bluetooth GATT event callback to be called whenever the value of a specific characteristic changes.
old-location: bltooth\bluetooth_gatt_notification_callback_function.htm
tech.root: bltooth
ms.assetid: 96AC4E49-76D7-47B5-93B9-64D574A28E0A
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BluetoothGattEventCallback, BluetoothGattEventCallback callback function [Bluetooth Devices], PFNBLUETOOTH_GATT_EVENT_CALLBACK, PFNBLUETOOTH_GATT_EVENT_CALLBACK callback, bltooth.bluetooth_gatt_notification_callback_function, bthledef/BluetoothGattEventCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: bthledef.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Supported in Windows 8 and later versions of Windows.
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - bthledef.h
api_name:
 - BluetoothGattEventCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNBLUETOOTH_GATT_EVENT_CALLBACK callback function


## -description


Profile drivers implement a Bluetooth GATT event callback to be called whenever the value of a specific characteristic changes.


## -parameters




### -param EventType [in]

The type of GATT event.


### -param EventOutParameter [in]

Pointer to a <a href="https://msdn.microsoft.com/EC6E5B85-495E-401B-ADE5-D51891A4BDFE">BLUETOOTH_GATT_VALUE_CHANGED_EVENT</a> structure.


### -param Context [in, optional]

The context specified by the profile driver in the <i>CallbackContext</i> parameter of 
      the <a href="https://msdn.microsoft.com/8C1477F8-8342-4405-8FE1-8109E6147EE9">BluetoothGATTRegisterEvent</a> function 
      when the profile driver registered the GATT callback function.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/EC6E5B85-495E-401B-ADE5-D51891A4BDFE">BLUETOOTH_GATT_VALUE_CHANGED_EVENT</a>



<a href="https://msdn.microsoft.com/6AF30DEA-2018-4AA2-B13A-BD31BD641F9F">BTH_LE_GATT_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/8C1477F8-8342-4405-8FE1-8109E6147EE9">BluetoothGATTRegisterEvent</a>
 

 

