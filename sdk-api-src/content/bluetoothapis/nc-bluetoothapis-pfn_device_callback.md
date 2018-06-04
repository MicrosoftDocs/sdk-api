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

# PFN_DEVICE_CALLBACK callback function


## -description


The <b>PFN_DEVICE_CALLBACK</b> function is a callback prototype used in association with selecting Bluetooth devices. The 
<b>PFN_DEVICE_CALLBACK</b> function can be set to <b>NULL</b> if no specialized filtering is required.


## -parameters




### -param pvParam

A parameter passed in from  the <b>pvParam</b> member of the 
<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS</a> structure through the <a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a> function.


### -param *pDevice

Remote Bluetooth address queried; this is the address inserted into the user-presented list of Bluetooth devices.


## -returns



Returning <b>FALSE</b> prevents the device from being added to the list view of Bluetooth devices.




## -remarks



The 
<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure pointed to in <i>pDevice</i> is the device that the 
<a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a> function is querying to determine if that device should be added to the list view.

If the callback performs SDP queries for each device, the list of devices from which the user can choose will be delayed until all devices can be queried. A recommended approach is to use the service to call bitfield in the class of device, available through <b>GET_COD_SERVICE</b>, to determine whether the device should be displayed to the user. The service class bitfield is available in the <b>pDevice</b> parameter through the <b>ulClassOfDevice</b> member.




## -see-also




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a>
 

 

