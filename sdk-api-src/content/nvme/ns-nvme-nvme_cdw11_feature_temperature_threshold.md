---
UID: NS:nvme.NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD
tech.root: fs
title: NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Temperature Threshold feature that is used to set an over temperature threshold and an under temperature threshold for up to nine temperature values.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD, *PNVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD
 - NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD
f1_keywords:
 - PNVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD
 - nvme/PNVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD
 - NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD
 - nvme/NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD structure


## -description

Contains parameters for the Temperature Threshold feature that is used to set an over temperature threshold and an under temperature threshold for up to nine temperature values.

The values from this structure are used in the **TemperatureThreshold** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

A controller may report up to nine temperature values in the [SMART / Health Information Log (NVME_HEALTH_INFO_LOG)](ns-nvme-nvme_health_info_log.md). For example, the Composite Temperature and Temperature Sensor 1 through Temperature Sensor 8. Associated with each implemented temperature sensor is an over temperature threshold and an under temperature threshold. When a temperature is greater than or equal to its corresponding over temperature threshold or less than or equal to its corresponding under temperature threshold, then bit one of the **CriticalWarning** field in the **NVME_HEALTH_INFO_LOG** structure is set to one. This may trigger an asynchronous event.

The over temperature threshold feature is implemented for Composite Temperature. The under temperature threshold Feature is implemented for Composite Temperature if a non-zero Warning Composite Temperature Threshold **WCTEMP** field value is reported in the Identify Controller [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md) data structure. The over temperature threshold and under temperature threshold features are implemented for all implemented temperature sensors (all Temperature Sensor fields that report a non-zero value).

The default value of the over temperature threshold feature for Composite Temperature is the value in the **WCTEMP** field in the **NVME_IDENTIFY_CONTROLLER_DATA** data structure if **WCTEMP** is non-zero; otherwise, it is implementation specific. The default value of the over temperature threshold for all implemented temperature sensors is `FFFFh`. The default value for all implemented under temperature thresholds is `0h`.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.TMPTH

Indicates the threshold for the temperature of the overall device (controller and NVM included) in units of Kelvin. This value is applied in a Set Features command and returned in a Get Features command, for the temperature sensor and threshold type specified.

### -field DUMMYSTRUCTNAME.TMPSEL

Specifies the temperature whose threshold is modified by a Set Features command and whose threshold value is returned by a Get Features command.

The following values are allowed for this field:

| Value              | Description                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------|
| `0000b`            | Composite Temperature                                                                               |
| `0001b`            | Temperature Sensor 1                                                                                |
| `0010b`            | Temperature Sensor 2                                                                                |
| `0011b`            | Temperature Sensor 3                                                                                |
| `0100b`            | Temperature Sensor 4                                                                                |
| `0101b`            | Temperature Sensor 5                                                                                |
| `0110b`            | Temperature Sensor 6                                                                                |
| `0111b`            | Temperature Sensor 7                                                                                |
| `1000b`            | Temperature Sensor 8                                                                                |
| `1001b` - `1110b`  | Reserved                                                                                            |
| `1111b`            | All implemented temperature sensors in a Set Features  command. Reserved in a Get Features command. |

### -field DUMMYSTRUCTNAME.THSEL

Specifies an [NVME_TEMPERATURE_THRESHOLD_TYPES](ne-nvme-nvme_temperature_threshold_types.md) value that indicates the threshold type that is modified by a Set Features command and whose threshold value is returned by a Get Features command.

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

## -see-also

- [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md)
- [NVME_TEMPERATURE_THRESHOLD_TYPES](ne-nvme-nvme_temperature_threshold_types.md)
- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)

