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

# GAMING_DEVICE_MODEL_INFORMATION structure


## -description


Contains information about the device that the game is running on.


## -struct-fields




### -field vendorId

The vendor of the device.


### -field deviceId

The type of device.


## -remarks



This is a Win32 API that's supported in both Win32 and UWP apps. While it works on any device family, it's only really of value on Xbox devices.




## -see-also




<a href="https://msdn.microsoft.com/bf210289-5963-4327-828b-98a0d14b5bfa">Gaming Device Information</a>



<a href="https://msdn.microsoft.com/78101CBA-63B5-4B3F-9CEC-A215F32D9EB8">GetGamingDeviceModelInformation function</a>
 

 

