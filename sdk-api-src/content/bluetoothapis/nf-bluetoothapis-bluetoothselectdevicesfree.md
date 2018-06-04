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

# BluetoothSelectDevicesFree function


## -description


The 
<b>BluetoothSelectDevicesFree</b> function frees resources associated with a previous call to 
<a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a>.


## -parameters




### -param pbtsdp

A pointer to a 
<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS</a> structure that identifies the Bluetooth device resources to free.


## -returns



Returns <b>TRUE</b> upon success. Returns <b>FALSE</b> if there are no resources to free.




## -remarks



Only call the <b>BluetoothSelectDevicesFree</b> function if a previous call to the <a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a> function returned <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a>
 

 

