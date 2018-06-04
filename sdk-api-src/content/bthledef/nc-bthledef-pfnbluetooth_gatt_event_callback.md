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
 

 

