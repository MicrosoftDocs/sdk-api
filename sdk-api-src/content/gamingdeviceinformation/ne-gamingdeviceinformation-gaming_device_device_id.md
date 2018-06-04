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

# GAMING_DEVICE_DEVICE_ID enumeration


## -description


Indicates the type of device that the game is running on.


## -enum-fields




### -field GAMING_DEVICE_DEVICE_ID_NONE

The device is not in the Xbox family.


### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE

The device is an Xbox One (original).


### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE_S

The device is an Xbox One S.


### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X

The device is an Xbox One X.


### -field GAMING_DEVICE_DEVICE_ID_XBOX_ONE_X_DEVKIT

The device is an Xbox One X dev kit.


## -remarks



This is a Win32 API that's supported in both Win32 and UWP apps. While it works on any device family, it's only really of value on Xbox devices.




## -see-also




<a href="https://msdn.microsoft.com/0D5A6358-0F82-4414-BD17-BDE22EDBBB15">GAMING_DEVICE_MODEL_INFORMATION structure</a>



<a href="https://msdn.microsoft.com/bf210289-5963-4327-828b-98a0d14b5bfa">Gaming Device Information</a>
 

 

