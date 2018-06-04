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

# _BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS structure


## -description


The <b>BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS</b> structure contains specific configuration information about the Bluetooth device responding to an authentication request.


## -struct-fields




### -field deviceInfo

A <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure that contains information about a Bluetooth device.


### -field authenticationMethod

A <a href="https://msdn.microsoft.com/2374df2c-2f50-4a06-aaad-384d81b067c5">BLUETOOTH_AUTHENTICATION_METHOD</a> enumeration that defines the authentication method utilized by the Bluetooth device.


### -field ioCapability

A <a href="https://msdn.microsoft.com/f1cd4fc9-5206-4f38-a2b9-621ca4c6ab86">BLUETOOTH_IO_CAPABILITY</a> enumeration that defines the input/output capabilities of the Bluetooth device.


### -field authenticationRequirements

A <a href="https://msdn.microsoft.com/644372af-d613-4fd6-adcd-7faf0afb0033">BLUETOOTH_AUTHENTICATION_REQUIREMENTS</a> specifies the 'Man in the Middle' protection required for authentication.


### -field Numeric_Value

A <b>ULONG</b> value used for Numeric Comparison authentication.


### -field Passkey

A <b>ULONG</b> value used as  the passkey used for authentication.


## -see-also




<a href="https://msdn.microsoft.com/644372af-d613-4fd6-adcd-7faf0afb0033">BLUETOOTH_AUTHENTICATION_REQUIREMENTS</a>



<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/f1cd4fc9-5206-4f38-a2b9-621ca4c6ab86">BLUETOOTH_IO_CAPABILITY</a>
 

 

