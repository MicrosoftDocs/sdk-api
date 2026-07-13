---
UID: NE:nvme.NVME_FEATURES
tech.root: fs
title: NVME_FEATURES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate which feature should be retrieved or configured by the **NVME_ADMIN_COMMAND_GET_FEATURES** and **NVME_ADMIN_COMMAND_SET_FEATURES** Admin commands.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_FEATURES
f1_keywords:
 - NVME_FEATURES
 - nvme/NVME_FEATURES
dev_langs:
 - c++
---

# NVME_FEATURES enumeration


## -description

Contains values that indicate which feature should be retrieved or configured by the **NVME_ADMIN_COMMAND_GET_FEATURES** and **NVME_ADMIN_COMMAND_SET_FEATURES** Admin commands.

## -enum-fields

### -field NVME_FEATURE_ARBITRATION

The Arbitration feature that controls command processing by defining the number of commands from a certain priority that may be executed.

### -field NVME_FEATURE_POWER_MANAGEMENT

The Power Management feature that allows the host to configure the power state.

### -field NVME_FEATURE_LBA_RANGE_TYPE

The Logical Block Addressing (LBA) Range Type feature that indicates the type and attributes of LBA ranges that are part of the specified namespace.

The LBA range information is used by a driver to determine if it can utilize a particular LBA range. The information is not exposed to higher level software.

### -field NVME_FEATURE_TEMPERATURE_THRESHOLD

The Temperature Threshold feature that maintains an over-temperature threshold or an under-temperature threshold for the nine temperature sensors.

### -field NVME_FEATURE_ERROR_RECOVERY

The Error Recovery feature that controls the error recovery attributes.

### -field NVME_FEATURE_VOLATILE_WRITE_CACHE

The Volatile Write Cache feature that controls whether the volatile write cache is enabled.

### -field NVME_FEATURE_NUMBER_OF_QUEUES

The Number of Queues feature that maintains the number of queues that the host requests for this controller.

### -field NVME_FEATURE_INTERRUPT_COALESCING

The Interrupt Coalescing feature that configures the interrupt coalescing settings for the controller.

### -field NVME_FEATURE_INTERRUPT_VECTOR_CONFIG

The Interrupt Vector Configuration feature that configures settings specific to a particular interrupt vector.

### -field NVME_FEATURE_WRITE_ATOMICITY

The Write Atomicity Normal feature that controls the operation of the Atomic Write Unit Normal (AWUN) and Namespace Atomic Write Unit Normal (NAWUN) parameters.

### -field NVME_FEATURE_ASYNC_EVENT_CONFIG

The Asynchronous Event Configuration feature that controls the events that trigger an asynchronous event notification to the host.

### -field NVME_FEATURE_AUTONOMOUS_POWER_STATE_TRANSITION

The Autonomous Power State Transition feature that configures the settings for autonomous power state transitions.

### -field NVME_FEATURE_HOST_MEMORY_BUFFER

The Host Memory Buffer feature that provides a mechanism for the host to allocate a portion of host memory for the controller to use exclusively.

### -field NVME_FEATURE_TIMESTAMP

The Timestamp feature.

### -field NVME_FEATURE_KEEP_ALIVE

The Keep Alive feature.

### -field NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT

The Controlled Thermal Management feature.

### -field NVME_FEATURE_NONOPERATIONAL_POWER_STATE

The Non-Operational Power State feature.

### -field NVME_FEATURE_NVM_SOFTWARE_PROGRESS_MARKER

The Software Progress Marker feature that indicates the load count of pre-boot software and is persistent across power states.

### -field NVME_FEATURE_NVM_HOST_IDENTIFIER

The Host Identifier feature that allows the host to register a Host Identifier with the controller.

The Host Identifier is used by the controller to determine whether other controllers in the NVM Subsystem are associated with the same host and is only required to be initialized if reservations are supported.

### -field NVME_FEATURE_NVM_RESERVATION_NOTIFICATION_MASK

The Reservation Notification Mask feature that controls the masking of reservation notifications on a per namespace basis.

### -field NVME_FEATURE_NVM_RESERVATION_PERSISTANCE

The Reservation Persistence feature that allows modification of the Persist Through Power Loss (PTPL) state.

## -remarks

In the **NVME_ADMIN_COMMAND_GET_FEATURES** and **NVME_ADMIN_COMMAND_SET_FEATURES** Admin commands, the feature is specified in the Feature Identifier (**FID**) member of the [NVME_CDW10_GET_FEATURES](ns-nvme-nvme_cdw10_get_features.md) and [NVME_CDW10_SET_FEATURES](ns-nvme-nvme_cdw10_set_features.md) structures.

## -see-also

[NVME_CDW10_GET_FEATURES](ns-nvme-nvme_cdw10_get_features.md)
[NVME_CDW10_SET_FEATURES](ns-nvme-nvme_cdw10_set_features.md)

