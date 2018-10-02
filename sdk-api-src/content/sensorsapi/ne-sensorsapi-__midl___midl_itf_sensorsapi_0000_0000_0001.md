---
UID: NE:sensorsapi.__MIDL___MIDL_itf_sensorsapi_0000_0000_0001
title: "__MIDL___MIDL_itf_sensorsapi_0000_0000_0001"
author: windows-sdk-content
description: Defines possible operational states for sensors.
old-location: winsensors_com_ref\sensorstate.htm
tech.root: SensorsAPI
ms.assetid: 4cf993ba-d767-4ef8-94a9-e819cc210360
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SENSOR_STATE_ACCESS_DENIED, SENSOR_STATE_ERROR, SENSOR_STATE_INITIALIZING, SENSOR_STATE_MAX, SENSOR_STATE_MIN, SENSOR_STATE_NOT_AVAILABLE, SENSOR_STATE_NO_DATA, SENSOR_STATE_READY, SensorState, SensorState enumeration, __MIDL___MIDL_itf_sensorsapi_0000_0000_0001, sensorsapi/SENSOR_STATE_ACCESS_DENIED, sensorsapi/SENSOR_STATE_ERROR, sensorsapi/SENSOR_STATE_INITIALIZING, sensorsapi/SENSOR_STATE_MAX, sensorsapi/SENSOR_STATE_MIN, sensorsapi/SENSOR_STATE_NOT_AVAILABLE, sensorsapi/SENSOR_STATE_NO_DATA, sensorsapi/SENSOR_STATE_READY, sensorsapi/SensorState, winsensors_com_ref.sensorstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - sensorsapi.h
api_name:
 - SensorState
product: Windows
targetos: Windows
req.typenames: SensorState
req.redist: 
---

# __MIDL___MIDL_itf_sensorsapi_0000_0000_0001 enumeration


## -description


Defines possible operational states for sensors.


## -enum-fields




### -field SENSOR_STATE_MIN

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

The sensor is available, but the user account does not have permission to access the sensor data. For more information about permissions, see <a href="https://msdn.microsoft.com/c755edcf-18c1-43d5-9dfe-c073e1f96b5f">Managing User Permissions</a>.


### -field SENSOR_STATE_ERROR

The sensor has raised an error.


### -field SENSOR_STATE_MAX

Maximum enumerated sensor state. Not a valid value.

