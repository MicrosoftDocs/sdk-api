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

# MagnetometerAccuracy enumeration


## -description


Specifies the accuracy of the magnetometer.


## -enum-fields




### -field MAGNETOMETER_ACCURACY_UNKNOWN


### -field MAGNETOMETER_ACCURACY_UNRELIABLE


### -field MAGNETOMETER_ACCURACY_APPROXIMATE


### -field MAGNETOMETER_ACCURACY_HIGH




#### - Approximate

The actual and reported values differ but may be accurate enough for some application. Apps that only need a relative value, like a virtual reality app, can continue without additional calibration. 


#### - High

The actual and reported values are accurate. No additional calibration is needed. 


#### - Unknown

This value is not used. 


#### - Unreliable

The reported values have a high degree of inaccuracy. Apps will typically ask the user to calibrate the device whenever this value is returned.


## -remarks



Apps that need calibration may periodically ask the user to calibrate the device. We suggest doing this no more than once every 10 minutes.



