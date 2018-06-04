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

# _BLUETOOTH_LOCAL_SERVICE_INFO structure


## -description


The <b>BLUETOOTH_LOCAL_SERVICE_INFO</b> structure contains local service information for a Bluetooth device. This structure is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536580">BluetoothSetLocalServiceInfo</a> function.


## -struct-fields




### -field Enabled

If <b>TRUE</b>, specifies that the advertised services are enabled; otherwise the advertised services are disabled.


### -field btAddr

A <a href="https://msdn.microsoft.com/2262a91b-c8b0-415a-9c23-7504998cc2a4">BLUETOOTH_ADDRESS</a> structure that contains the address of a remote device. This address is used when advertising services to a device.


### -field szName

The service name. The maximum length of this string, including the null terminator, is <b>BLUETOOTH_MAX_SERVICE_NAME_SIZE</b> (256).


### -field szDeviceString

The local device name, if any, such as  COM4 or LPT1. The maximum length of this string, including the null terminator, is <b>BLUETOOTH_DEVICE_NAME_SIZE</b> (256).


## -remarks



In the event  the service is not associated with a specific device, <b>btAddr</b> should be set to <b>BTH_ADDR_NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536580">BluetoothSetLocalServiceInfo</a>
 

 

