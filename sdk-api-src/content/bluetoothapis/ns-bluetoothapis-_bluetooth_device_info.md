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

# _BLUETOOTH_DEVICE_INFO structure


## -description


The 
<b>BLUETOOTH_DEVICE_INFO</b> structure provides information about a Bluetooth device.


## -struct-fields




### -field dwSize

Size of the 
<b>BLUETOOTH_DEVICE_INFO</b> structure, in bytes.


### -field Address

Address of the device.


### -field ulClassofDevice

Class of the device.


### -field fConnected

Specifies whether the device is connected.


### -field fRemembered

Specifies whether the device is a remembered device. Not all remembered devices are authenticated.


### -field fAuthenticated

Specifies whether the device is authenticated, paired, or bonded. All authenticated devices are remembered.


### -field stLastSeen

Last time the device was seen, in the form of a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure.


### -field stLastUsed

Last time the device was used, in the form of a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure.


### -field szName

Name of the device.


## -remarks



See the Bluetooth specification at 
<a href="https://www.bluetooth.org/Technical/AssignedNumbers/references.htm">https://www.bluetooth.org/Technical/AssignedNumbers/references.htm</a> for class of device (COD) information.




## -see-also




<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>
 

 

