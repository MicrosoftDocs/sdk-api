---
UID: NS:nvme.NVME_CDW11_FEATURES
tech.root: fs
title: NVME_CDW11_FEATURES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Get Features and Set Features commands that retrieve or set the attributes of the specified feature.
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
req.typenames: NVME_CDW11_FEATURES, *PNVME_CDW11_FEATURES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURES
 - NVME_CDW11_FEATURES
f1_keywords:
 - PNVME_CDW11_FEATURES
 - nvme/PNVME_CDW11_FEATURES
 - NVME_CDW11_FEATURES
 - nvme/NVME_CDW11_FEATURES
dev_langs:
 - c++
---

# NVME_CDW11_FEATURES structure


## -description

Contains parameters for the Get Features and Set Features commands that retrieve or set the attributes of the specified feature.

This structure is used in the **CDW11** parameter of the **GETFEATURES** and **SETFEATURES** fields in the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field NumberOfQueues

Specifies an [NVME_CDW11_FEATURE_NUMBER_OF_QUEUES](ns-nvme-nvme_cdw11_feature_number_of_queues.md) structure containing values that indicates the number of queues that the host requests for this controller.

When a Set Features or Get Features command is submitted for the Number of Queues Feature, the **NVME_CDW11_FEATURE_NUMBER_OF_QUEUES** structure is returned in the Dword 0 (**DW0**) field of the [Completion Queue entry](ns-nvme-nvme_completion_entry.md) for that command.

### -field AsUlong

### -field InterruptCoalescing

Specifies an [NVME_CDW11_FEATURE_INTERRUPT_COALESCING](ns-nvme-nvme_cdw11_feature_interrupt_coalescing.md) structure containing values that configure the interrupt coalescing settings.

When a Get Features command is submitted for the Interrupt Coalescing Feature, the values specified in the **TIME** and **THR** fields of the **NVME_CDW11_FEATURE_INTERRUPT_COALESCING** structure are returned in the **DW0** field of the [Completion Queue Entry](ns-nvme-nvme_completion_entry.md) for that command.

### -field InterruptVectorConfig

Specifies an [NVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG](ns-nvme-nvme_cdw11_feature_interrupt_vector_config.md) structure containing values that configure settings specific to a particular interrupt vector.

When a Get Features command is submitted for the Interrupt Vector Configuration Feature, the values specified in the Interrupt Vector (**IV**) and Coalescing Disabled (**CD**) fields of the **NVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG** structure are returned in the **DW0** field of the [Completion Queue Entry](ns-nvme-nvme_completion_entry.md) for that command.

Prior to issuing this feature, the host should configure the specified Interrupt Vector with a valid I/O Completion Queue. If the I/O Completion Queue or Interrupt Vector specified is invalid, the controller will return a status of [NVME_STATUS_INVALID_FIELD_IN_COMMAND](ne-nvme-nvme_status_generic_command_codes.md).

### -field LbaRangeType

Specifies an [NVME_CDW11_FEATURE_LBA_RANGE_TYPE](ns-nvme-nvme_cdw11_feature_lba_range_type.md) structure containing a value that specifies the number of LBA ranges for the LBA Range Type Feature in the Set Features command.

This field is used for the Set Features command only and is ignored for the Get Features command.

The LBA Range Type feature specifies type and attributes of Logical Block Allocation (LBA) ranges that are part of the specified namespace. The feature uses the **NVME_CDW11_FEATURE_LBA_RANGE_TYPE** structure to specify the number of LBA ranges, and the [NVME_LBA_RANGET_TYPE_ENTRY](ns-nvme-nvme_lba_ranget_type_entry.md) data structure to specify the type and attribute information.

When a Get Features command is submitted for the LBA Range Type feature, the value specified in the **NUM** field of the **NVME_CDW11_FEATURE_LBA_RANGE_TYPE** structure is returned in the **DW0** field of the [Completion Queue entry](ns-nvme-nvme_completion_entry.md), and the LBA Range Type [NVME_LBA_RANGET_TYPE_ENTRY](ns-nvme-nvme_lba_ranget_type_entry.md) data structure is returned in the data buffer for that command.

### -field Arbitration

Specifies an [NVME_CDW11_FEATURE_ARBITRATION](ns-nvme-nvme_cdw11_feature_arbitration.md) structure containing values that control command arbitration.

When a Get Features command is submitted for the Arbitration feature, the structure specified in this field is returned in the **DW0** field of the [Completion Queue entry](ns-nvme-nvme_completion_entry.md) for that command.

### -field VolatileWriteCache

Specifies an [NVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE](ns-nvme-nvme_cdw11_feature_volatile_write_cache.md) structure containing values that control the volatile write cache, if present, on the controller.

When a Get Features command is submitted for the Volatile Write Cache Feature, the value specified in the **WCE** field of the **NVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE** is returned in the **DW0** field of the [Completion Queue Entry](ns-nvme-nvme_completion_entry.md) for that command.

### -field AsyncEventConfig

Specifies an [NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG](ns-nvme-nvme_cdw11_feature_async_event_config.md) structure containing parameters for the Asynchronous Event Configuration Feature that controls the events that trigger an asynchronous event notification to the host.

When a Get Features command is submitted for the Asynchronous Event Configuration Feature, the values specified in The **NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG** structure are returned in the **DW0** field of the [Completion Queue Entry](ns-nvme-nvme_completion_entry.md) structure for that command.

### -field PowerManagement

Specifies an [NVME_CDW11_FEATURE_POWER_MANAGEMENT](ns-nvme-nvme_cdw11_feature_power_management.md) structure containing values that allow the host to configure the power state.

When a Get Features command is submitted for the Power Management feature, the **NVME_CDW11_FEATURE_POWER_MANAGEMENT** structure is returned in the **DW0** field of the [Completion Queue entry](ns-nvme-nvme_completion_entry.md) for that command.

### -field AutoPowerStateTransition

Specifies an [NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION](ns-nvme-nvme_cdw11_feature_auto_power_state_transition.md) structure containing parameters for the Autonomous Power State Transition Feature that configures the settings for autonomous power state transitions.

The Autonomous Power State Transition Feature specifies the attribute information in the **NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION** data structure and the [Autonomous Power State Transition Entry](ns-nvme-nvme_auto_power_state_transition_entry.md) data structure.

When a Get Features command is submitted for the Autonomous Power State Transition Feature, the value specified in The **APSTE** field of the **NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION** structure is returned in the **DW0** field of the [Completion Queue Entry](ns-nvme-nvme_completion_entry.md), and the [NVME_AUTO_POWER_STATE_TRANSITION_ENTRY](ns-nvme-nvme_auto_power_state_transition_entry.md) data structure is returned in the data buffer for that command.

### -field TemperatureThreshold

Specifies an [NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD](ns-nvme-nvme_cdw11_feature_temperature_threshold.md) structure containing values that are used to set or retrieve temperature threshold values for the controller.

### -field HostMemoryBuffer

Specifies an [NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw11_feature_temperature_threshold.md) structure containing values that are used to control the Host Memory Buffer.

The Host Memory Buffer feature provides a mechanism for the host to allocate a portion of host memory for the controller to use exclusively. After a successful completion of a Set Features command that enables the host memory buffer, the host will not write to the associated host memory region, buffer size, or descriptor list until the host memory buffer has been disabled. After a successful completion of a Set Features command that disables the host memory buffer, the controller will not access any data in the host memory buffer until the host memory buffer has been enabled.

The *Host Memory Descriptor List* is a physically contiguous data structure in host memory that describes the address and length pairs of the Host Memory Buffer. The boundaries and contents of the list are defined in following fields and structures:

- The lower bounds of the Host Memory Descriptor List address are defined in the **HMDLLA** field of the [NVME_CDW13_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw13_feature_host_memory_buffer.md).
- The upper bounds of the Host Memory Descriptor List address are defined in the **HMDLUA** field of the [NVME_CDW14_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw14_feature_host_memory_buffer.md).
- The number of addresses and length pairs for the Host Memory Descriptor List are specified in the Host Memory Descriptor List Entry Count in the **HMDLEC** field of the [NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw15_feature_host_memory_buffer.md). 
- The fields for an entry in the Host Memory Descriptor List are specified in the [NVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY](ns-nvme-nvme_host_memory_buffer_descriptor_entry.md) structure.

### -field WriteAtomicityNormal

Specifies an [NVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL](ns-nvme-nvme_cdw11_feature_write_atomicity_normal.md) structure containing values that control the operation of the Atomic Write Unit Normal (AWUN) and Namespace Atomic Write Unit Normal (NAWUN) parameters that define the controller’s support for atomic operations.

When a Get Features command is submitted for the Write Atomicity Normal Feature, the values specified in The **NVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL** structure are returned in the **DW0** field of the [Completion Queue Entry](ns-nvme-nvme_completion_entry.md) structure for that command.

### -field NonOperationalPowerState

Specifies an [NVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE](ns-nvme-nvme_cdw11_feature_non_operational_power_state.md) structure containing values for the Non-Operational Power State Feature that indicates whether permissive mode is enabled for a non-operational power state.

## -remarks

## -see-also

- [NVME_COMMAND](ns-nvme-nvme_command.md)
- [NVME_CDW10_GET_FEATURES](ns-nvme-nvme_cdw10_get_features.md)
- [NVME_CDW10_SET_FEATURES](ns-nvme-nvme_cdw10_set_features.md)
- [NVME_CDW12_FEATURES](ns-nvme-nvme_cdw12_features.md)
- [NVME_CDW13_FEATURES](ns-nvme-nvme_cdw13_features.md)
- [NVME_CDW14_FEATURES](ns-nvme-nvme_cdw14_features.md)
- [NVME_CDW15_FEATURES](ns-nvme-nvme_cdw15_features.md)

