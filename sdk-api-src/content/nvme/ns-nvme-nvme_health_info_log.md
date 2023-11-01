---
UID: NS:nvme.NVME_HEALTH_INFO_LOG
tech.root: fs
title: NVME_HEALTH_INFO_LOG
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify the information contained in the SMART / Health Information Log page.
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
req.typenames: NVME_HEALTH_INFO_LOG, *PNVME_HEALTH_INFO_LOG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_HEALTH_INFO_LOG
 - NVME_HEALTH_INFO_LOG
f1_keywords:
 - PNVME_HEALTH_INFO_LOG
 - nvme/PNVME_HEALTH_INFO_LOG
 - NVME_HEALTH_INFO_LOG
 - nvme/NVME_HEALTH_INFO_LOG
dev_langs:
 - c++
---

# NVME_HEALTH_INFO_LOG structure


## -description

Contains fields that specify the information contained in the SMART / Health Information Log page.

The SMART / Health Information Log page provides SMART and general health information over the life of the controller that is retained across power cycles. The log page is supported on a global basis. To request the global log page, specify the namespace `FFFFFFFFh`.

The SMART / Health Information Log page may also be supported on a per namespace basis, as indicated in the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure. If the log page is not supported on a per namespace basis, specifying any namespace other than `FFFFFFFFh` should abort the command with a status of [NVME_STATUS_INVALID_FIELD_IN_COMMAND](ne-nvme-nvme_status_generic_command_codes.md). In NVMe version 1.3, there is no namespace specific information defined in the SMART / Health log page, thus the global log page and namespaces specific log page contain identical information.

Critical warnings regarding the health of the NVM subsystem are indicated via an asynchronous event notification to the host. The warnings that results in an asynchronous event notification to the host are configured using the [Set Features command](ns-nvme-nvme_cdw10_set_features.md).

Performance may be calculated using parameters returned as part of the SMART / Health Information log. Specifically, the number of Read or Write commands, the amount of data read or written, and the amount of controller busy time enables both I/Os per second and bandwidth to be calculated.

The **NVME_HEALTH_INFO_LOG** structure is returned by the Get Log Page command. For more information, see [NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md).

## -struct-fields

### -field CriticalWarning

A Critical Warning (**CriticalWarning**) structure containing fields that indicate critical warnings for the state of the controller.

Each field of the **CriticalWarning** structure is a bit that corresponds to a critical warning type; multiple bits may be set. If a bit is cleared to `0`, then that critical warning does not apply. Bits in this field represent the current associated state and are not persistent.

Critical warnings may result in an asynchronous event notification to the host.

### -field CriticalWarning.DUMMYSTRUCTNAME

### -field CriticalWarning.DUMMYSTRUCTNAME.AvailableSpaceLow

Indicates whether the available spare space has fallen below the threshold.

When this value is set to `1`, the available spare space has fallen below the threshold.

### -field CriticalWarning.DUMMYSTRUCTNAME.TemperatureThreshold

Indicates whether a temperature is above an over temperature threshold or below an under temperature threshold.

When this value is set to `1`, a temperature is above an over temperature threshold or below an under temperature threshold. For more information about temperature thresholds, see [NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD](ns-nvme-nvme_cdw11_feature_temperature_threshold.md).

### -field CriticalWarning.DUMMYSTRUCTNAME.ReliabilityDegraded

Indicates whether the NVM subsystem reliability has been degraded.

When this value is set to `1`, the NVM subsystem reliability has been degraded due to significant media related errors or any internal error that degrades NVM subsystem reliability.

### -field CriticalWarning.DUMMYSTRUCTNAME.ReadOnly

Indicates whether the media has been placed in read only mode.

When this value is set to `1`, then the media has been placed in read only mode.

### -field CriticalWarning.DUMMYSTRUCTNAME.VolatileMemoryBackupDeviceFailed

Indicates whether the volatile memory backup device has failed.

When this value is set to `1`, then the volatile memory backup device has failed. This field is only valid if the controller has a volatile memory backup solution.

### -field CriticalWarning.DUMMYSTRUCTNAME.Reserved

Bits 05:07 of the **CriticalWarning** structure are reserved.

### -field CriticalWarning.AsUchar

### -field Temperature

Indicates the composite temperature, in degrees Kelvin, of the overall device, including the controller and the NVM subsystem.

If the temperature in this field exceeds the temperature threshold, an asynchronous event completion may occur. For more information, see [NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD](ns-nvme-nvme_cdw11_feature_temperature_threshold.md).

Warning and critical overheating composite temperature threshold values are reported by the **WCTEMP** and **CCTEMP** fields in the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure.

### -field AvailableSpare

Indicates a normalized percentage (0 to 100) of the remaining spare capacity available.

### -field AvailableSpareThreshold

Indicates the threshold of available spare capacity.

When the value of **AvailableSpare** falls below the threshold indicated in this field, an asynchronous event completion may occur. The value is indicated as a normalized percentage (0 to 100).

### -field PercentageUsed

Indicates a vendor specific estimate of the percentage of NVM subsystem life used, based on the actual usage and the manufacturer’s prediction of NVM life.

A value of 100 indicates that the estimated endurance of the NVM in the NVM subsystem has been consumed, but may not indicate an NVM subsystem failure. The value is allowed to exceed 100. Percentages greater than 254 are represented as 255. This value is updated once per power-on hour (when the controller is not in a sleep state).

### -field Reserved0

A reserved field.

### -field DataUnitRead

Indicates the number of 512 byte data units the host has read from the controller, not including metadata.

The value of this field is reported in thousands and is rounded up. For example, a value of 1 corresponds to 1000 units of 512 bytes read. When the Logical Block Access (LBA) size is a value other than 512 bytes, the controller converts the amount of data read to 512 byte units.

For the NVM command set, logical blocks read as part of Compare and Read operations are included in this value.

### -field DataUnitWritten

Indicates the number of 512 byte data units the host has written to the controller, not including metadata.

The value of this field is reported in thousands and is rounded up. For example, a value of 1 corresponds to 1000 units of 512 bytes read. When the Logical Block Access (LBA) size is a value other than 512 bytes, the controller converts the amount of data written to 512 byte units.

For the NVM command set, logical blocks written as part of Write operations are included in this value. Write Uncorrectable commands do not impact this value.

### -field HostReadCommands

Indicates the number of Read commands completed by the controller.

For the NVM command set, this is the number of Compare and Read commands.

### -field HostWrittenCommands

Indicates the number of Write commands completed by the controller.

For the NVM command set, this is the number of Write commands.

### -field ControllerBusyTime

Indicates the amount of time, in minutes, that the controller is busy with I/O commands.

The controller is busy when there is a command outstanding to an I/O Queue. Specifically, when a command was issued via an I/O [Submission Queue Tail doorbell](ns-nvme-nvme_submission_queue_tail_doorbell.md) write and the corresponding completion queue entry has not been posted yet to the associated I/O Completion Queue.

### -field PowerCycle

Indicates the number of power cycles.

### -field PowerOnHours

Indicates the number of power-on hours. This does not include time that the controller was powered and in a low power state condition.

### -field UnsafeShutdowns

Indicates the number of unsafe shutdowns. This count is incremented when a shutdown notification, indicated in the **SHN** filed of [Controller Configuration](ns-nvme-nvme_controller_configuration.md), is not received prior to loss of power.

### -field MediaErrors

Indicates the number of occurrences where the controller detected an unrecovered data integrity error.

[Media Errors](ne-nvme-nvme_status_media_error_codes.md) such as uncorrectable ECC, CRC checksum failure, or LBA tag mismatch are included in this field.

### -field ErrorInfoLogEntryCount

Indicates the number of [Error Information](ns-nvme-nvme_error_info_log.md) log entries over the life of the controller.

### -field WarningCompositeTemperatureTime

Indicates the amount of time, in minutes, that the controller is operational and the [Composite Temperature (**Temperature**)](#-field-temperature) is greater than or equal to the Warning Composite Temperature Threshold (**WCTEMP**) field and less than the Critical Composite Temperature Threshold (**CCTEMP**) field in the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure.

If the value of the **WCTEMP** or **CCTEMP** field is `0h`, then this field is always cleared to `0h` regardless of the **Temperature** value.

### -field CriticalCompositeTemperatureTime

Indicates the amount of time in minutes that the controller is operational and the [Composite Temperature (**Temperature**)](#-field-temperature) is greater the Critical Composite Temperature Threshold (**CCTEMP**) field in the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure.

If the value of the **CCTEMP** field is `0h`, then this field is always cleared to `0h` regardless of the **Temperature** value.

### -field TemperatureSensor1

Indicates the current temperature in degrees Kelvin reported by temperature sensor 1.

### -field TemperatureSensor2

Indicates the current temperature in degrees Kelvin reported by temperature sensor 2.

### -field TemperatureSensor3

Indicates the current temperature in degrees Kelvin reported by temperature sensor 3.

### -field TemperatureSensor4

Indicates the current temperature in degrees Kelvin reported by temperature sensor 4.

### -field TemperatureSensor5

Indicates the current temperature in degrees Kelvin reported by temperature sensor 5.

### -field TemperatureSensor6

Indicates the current temperature in degrees Kelvin reported by temperature sensor 6.

### -field TemperatureSensor7

Indicates the current temperature in degrees Kelvin reported by temperature sensor 7.

### -field TemperatureSensor8

Indicates the current temperature in degrees Kelvin reported by temperature sensor 8.

### -field Reserved1

A reserved field.

## -remarks

The temperature reported by a temperature sensor may be used to trigger an asynchronous event. For more information, see [NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD](ns-nvme-nvme_cdw11_feature_temperature_threshold.md).

## -see-also

- [NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD](ns-nvme-nvme_cdw11_feature_temperature_threshold.md)

