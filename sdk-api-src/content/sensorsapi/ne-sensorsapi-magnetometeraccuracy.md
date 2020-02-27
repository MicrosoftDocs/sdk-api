---
UID: NE:sensorsapi.MagnetometerAccuracy
title: MagnetometerAccuracy (sensorsapi.h)
description: Specifies the accuracy of the magnetometer.
old-location: winsensors\magnetometeraccuracy.htm
tech.root: SensorsAPI
ms.assetid: DBD06A2E-35AB-4692-8475-98B803C2202B
ms.date: 12/05/2018
ms.keywords: Approximate, High, MagnetometerAccuracy, MagnetometerAccuracy enumeration [WinSensors], Unknown, Unreliable, sensorsapi/Approximate, sensorsapi/High, sensorsapi/MagnetometerAccuracy, sensorsapi/Unknown, sensorsapi/Unreliable, winsensors.magnetometeraccuracy
f1_keywords:
- sensorsapi/MagnetometerAccuracy
dev_langs:
- c++
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- sensorsapi.h
api_name:
- MagnetometerAccuracy
targetos: Windows
req.typenames: MagnetometerAccuracy
req.redist: 
ms.custom: 19H1
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



