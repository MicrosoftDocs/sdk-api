---
UID: NE:sensorsapi.LOCATION_DESIRED_ACCURACY
title: LOCATION_DESIRED_ACCURACY (sensorsapi.h)
description: The LOCATION_DESIRED_ACCURACY enumeration type defines values for the SENSOR_PROPERTY_LOCATION_DESIRED_ACCURACY property.
helpviewer_keywords: ["LOCATION_DESIRED_ACCURACY","LOCATION_DESIRED_ACCURACY enumeration [Sensor Devices]","LOCATION_DESIRED_ACCURACY_DEFAULT","LOCATION_DESIRED_ACCURACY_HIGH","Sensor_Enums_a794ec29-a465-4d6a-b32e-c5eb890c95ae.xml","sensors.location_desired_accuracy","sensorsapi/LOCATION_DESIRED_ACCURACY","sensorsapi/LOCATION_DESIRED_ACCURACY_DEFAULT","sensorsapi/LOCATION_DESIRED_ACCURACY_HIGH"]
old-location: sensors\location_desired_accuracy.htm
tech.root: sensors
ms.assetid: 21eefb20-b5ad-43c7-a1aa-92731c856363
ms.date: 12/05/2018
ms.keywords: LOCATION_DESIRED_ACCURACY, LOCATION_DESIRED_ACCURACY enumeration [Sensor Devices], LOCATION_DESIRED_ACCURACY_DEFAULT, LOCATION_DESIRED_ACCURACY_HIGH, Sensor_Enums_a794ec29-a465-4d6a-b32e-c5eb890c95ae.xml, sensors.location_desired_accuracy, sensorsapi/LOCATION_DESIRED_ACCURACY, sensorsapi/LOCATION_DESIRED_ACCURACY_DEFAULT, sensorsapi/LOCATION_DESIRED_ACCURACY_HIGH
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
targetos: Windows
req.typenames: LOCATION_DESIRED_ACCURACY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LOCATION_DESIRED_ACCURACY
 - sensorsapi/LOCATION_DESIRED_ACCURACY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SensorsApi.h
api_name:
 - LOCATION_DESIRED_ACCURACY
---

# LOCATION_DESIRED_ACCURACY enumeration


## -description

The <b>LOCATION_DESIRED_ACCURACY </b> enumeration type defines values for the <a href="/windows-hardware/drivers/sensors/sensor-properties2">SENSOR_PROPERTY_LOCATION_DESIRED_ACCURACY</a> property.

## -enum-fields

### -field LOCATION_DESIRED_ACCURACY_DEFAULT:0

Indicates that the sensor should use the accuracy for which it can optimize power and other such cost considerations.

### -field LOCATION_DESIRED_ACCURACY_HIGH

Indicates that the sensor should deliver the highest-accuracy report possible. This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/sensorsclassextension/nf-sensorsclassextension-isensordriver-ongetproperties">ISensorDriver::OnGetProperties</a>
