---
UID: NE:sensorsapi.LOCATION_DESIRED_ACCURACY
title: LOCATION_DESIRED_ACCURACY
author: windows-sdk-content
description: The LOCATION_DESIRED_ACCURACY enumeration type defines values for the SENSOR_PROPERTY_LOCATION_DESIRED_ACCURACY property.
old-location: sensors\location_desired_accuracy.htm
tech.root: sensors
ms.assetid: 21eefb20-b5ad-43c7-a1aa-92731c856363
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LOCATION_DESIRED_ACCURACY, LOCATION_DESIRED_ACCURACY enumeration [Sensor Devices], LOCATION_DESIRED_ACCURACY_DEFAULT, LOCATION_DESIRED_ACCURACY_HIGH, Sensor_Enums_a794ec29-a465-4d6a-b32e-c5eb890c95ae.xml, sensors.location_desired_accuracy, sensorsapi/LOCATION_DESIRED_ACCURACY, sensorsapi/LOCATION_DESIRED_ACCURACY_DEFAULT, sensorsapi/LOCATION_DESIRED_ACCURACY_HIGH
ms.topic: enum
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7,Available in Windows 7.
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
 - SensorsApi.h
api_name:
 - LOCATION_DESIRED_ACCURACY
product: Windows
targetos: Windows
req.typenames: LOCATION_DESIRED_ACCURACY
req.redist: 
---

# LOCATION_DESIRED_ACCURACY enumeration


## -description


The <b>LOCATION_DESIRED_ACCURACY </b>enumeration type defines values for the <a href="https://msdn.microsoft.com/1BF1568D-A889-4158-9C6D-160D9B06F0DE">SENSOR_PROPERTY_LOCATION_DESIRED_ACCURACY</a> property.


## -enum-fields




### -field LOCATION_DESIRED_ACCURACY_DEFAULT

Indicates that the sensor should use the accuracy for which it can optimize power and other such cost considerations.


### -field LOCATION_DESIRED_ACCURACY_HIGH

Indicates that the sensor should deliver the highest-accuracy report possible. This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.


## -see-also




<a href="https://msdn.microsoft.com/8c7f378c-b4e6-4074-8b6a-571068b5ab80">ISensorDriver::OnGetProperties</a>
 

 

