---
UID: NC:bthledef.PFNBLUETOOTH_GATT_EVENT_CALLBACK
title: PFNBLUETOOTH_GATT_EVENT_CALLBACK
author: windows-sdk-content
description: Profile drivers implement a Bluetooth GATT event callback to be called whenever the value of a specific characteristic changes.
old-location: bltooth\bluetooth_gatt_notification_callback_function.htm
old-project: bltooth
ms.assetid: 96AC4E49-76D7-47B5-93B9-64D574A28E0A
ms.author: windowssdkdev
ms.date: 04/27/2018
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
tech.root: 
req.typenames: BTH_RADIO_IN_RANGE, *PBTH_RADIO_IN_RANGE
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
req.lib: 
req.dll: 
req.irql: 
---

# PFNBLUETOOTH_GATT_EVENT_CALLBACK callback function


## -description


Profile drivers implement a Bluetooth GATT event callback to be called whenever the value of a specific characteristic changes.


## -parameters




### -param EventType [in]

The type of GATT event.


### -param EventOutParameter [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt188598">BLUETOOTH_GATT_VALUE_CHANGED_EVENT</a> structure.


### -param Context [in, optional]

The context specified by the profile driver in the <i>CallbackContext</i> parameter of 
      the <a href="https://msdn.microsoft.com/library/windows/hardware/hh450804">BluetoothGATTRegisterEvent</a> function 
      when the profile driver registered the GATT callback function.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt188598">BLUETOOTH_GATT_VALUE_CHANGED_EVENT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450849">BTH_LE_GATT_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450804">BluetoothGATTRegisterEvent</a>
 

 

