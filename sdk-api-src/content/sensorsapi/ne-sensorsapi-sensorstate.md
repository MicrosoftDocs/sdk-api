---
UID: NE:sensorsapi.__MIDL___MIDL_itf_sensorsapi_0000_0000_0001
title: SensorState (sensorsapi.h)
description: Defines possible operational states for sensors.
helpviewer_keywords: ["SENSOR_STATE_ACCESS_DENIED","SENSOR_STATE_ERROR","SENSOR_STATE_INITIALIZING","SENSOR_STATE_MAX","SENSOR_STATE_MIN","SENSOR_STATE_NOT_AVAILABLE","SENSOR_STATE_NO_DATA","SENSOR_STATE_READY","SensorState","SensorState enumeration","sensorsapi/SENSOR_STATE_ACCESS_DENIED","sensorsapi/SENSOR_STATE_ERROR","sensorsapi/SENSOR_STATE_INITIALIZING","sensorsapi/SENSOR_STATE_MAX","sensorsapi/SENSOR_STATE_MIN","sensorsapi/SENSOR_STATE_NOT_AVAILABLE","sensorsapi/SENSOR_STATE_NO_DATA","sensorsapi/SENSOR_STATE_READY","sensorsapi/SensorState","winsensors_com_ref.sensorstate"]
old-location: winsensors_com_ref\sensorstate.htm
tech.root: winsensors
ms.assetid: 4cf993ba-d767-4ef8-94a9-e819cc210360
ms.date: 12/05/2018
ms.keywords: SENSOR_STATE_ACCESS_DENIED, SENSOR_STATE_ERROR, SENSOR_STATE_INITIALIZING, SENSOR_STATE_MAX, SENSOR_STATE_MIN, SENSOR_STATE_NOT_AVAILABLE, SENSOR_STATE_NO_DATA, SENSOR_STATE_READY, SensorState, SensorState enumeration, sensorsapi/SENSOR_STATE_ACCESS_DENIED, sensorsapi/SENSOR_STATE_ERROR, sensorsapi/SENSOR_STATE_INITIALIZING, sensorsapi/SENSOR_STATE_MAX, sensorsapi/SENSOR_STATE_MIN, sensorsapi/SENSOR_STATE_NOT_AVAILABLE, sensorsapi/SENSOR_STATE_NO_DATA, sensorsapi/SENSOR_STATE_READY, sensorsapi/SensorState, winsensors_com_ref.sensorstate
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.typenames: SensorState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_sensorsapi_0000_0000_0001
 - sensorsapi/__MIDL___MIDL_itf_sensorsapi_0000_0000_0001
 - SensorState
 - sensorsapi/SensorState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - sensorsapi.h
api_name:
 - SensorState
---

# SensorState enumeration


## -description

Defines possible operational states for sensors.

## -enum-fields

### -field SENSOR_STATE_MIN:0

Minimum enumerated sensor state. Use <b>SENSOR_STATE_READY</b> instead.

### -field SENSOR_STATE_READY

Ready to send sensor data.

### -field SENSOR_STATE_NOT_AVAILABLE

The sensor is not available for use.

### -field SENSOR_STATE_NO_DATA

The sensor is available but does not have data.

### -field SENSOR_STATE_INITIALIZING

The sensor is available, but performing initialization. Try again later.

### -field SENSOR_STATE_ACCESS_DENIED

The sensor is available, but the user account does not have permission to access the sensor data. For more information about permissions, see <a href="/windows/desktop/SensorsAPI/managing-user-permissions">Managing User Permissions</a>.

### -field SENSOR_STATE_ERROR

The sensor has raised an error.

### -field SENSOR_STATE_MAX

Maximum enumerated sensor state. Not a valid value.
