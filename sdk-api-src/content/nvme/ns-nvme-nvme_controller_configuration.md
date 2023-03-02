---
UID: NS:nvme.NVME_CONTROLLER_CONFIGURATION
tech.root: fs
title: NVME_CONTROLLER_CONFIGURATION
ms.date: 08/09/2022
ms.topic: language-reference
targetos: Windows
description: Contains read/write configuration settings for the controller.
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
req.typenames: NVME_CONTROLLER_CONFIGURATION, *PNVME_CONTROLLER_CONFIGURATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CONTROLLER_CONFIGURATION
 - NVME_CONTROLLER_CONFIGURATION
f1_keywords:
 - PNVME_CONTROLLER_CONFIGURATION
 - nvme/PNVME_CONTROLLER_CONFIGURATION
 - NVME_CONTROLLER_CONFIGURATION
 - nvme/NVME_CONTROLLER_CONFIGURATION
dev_langs:
 - c++
---

# NVME_CONTROLLER_CONFIGURATION structure


## -description

Contains read/write configuration settings for the controller.

The host software sets the following fields to valid values prior to enabling the controller by setting the [Enable **EN**](#field-dummystructname.en) field value to `1`:

- [Arbitration Mechanism **AMS**](#field-dummystructname.ams)
- [Memory Page Size **MPS**](#field-dummystructname.mps)
- [Command Set **CSS**](#field-Sdummystructname.css)

This structure is used in the Controller Capabilities (**CC**) field of the [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.EN

Indicates whether the controller is enabled to process commands.

When this value is set to `1`, the controller will process commands based on [Submission Queue Tail Doorbell](ns-nvme-nvme_submission_queue_tail_doorbell.md) writes.
When this value is cleared to `0`, the controller will not process commands nor post [Completion Queue entries](ns-nvme-nvme_completion_entry.md) to Completion Queues.

When this field transitions from `1` to `0`, the controller is reset (referred to as a Controller Reset). The reset deletes all I/O Submission Queues and I/O Completion Queues, resets the Admin Submission Queue and Completion Queue, and brings the hardware to an idle state. The reset does not affect PCI Express registers or the Admin Queue registers (AQA, ASQ, or ACQ). All other controller registers and internal controller states (such as, Feature values that are not persistent across power states) are reset to their default values. The controller ensures that there is no data loss for commands that have had corresponding Completion Queue entries posted to an I/O Completion Queue prior to the reset operation.

When this field is cleared to `0`, the value of the Ready (**RDY**) field in [Controller Status](ns-nvme-nvme_controller_status.md) is cleared to `0` by the controller once the controller is ready to be re-enabled. When this field is set to `1`, the controller sets the value of the **RDY** field in [Controller Status](ns-nvme-nvme_controller_status.md) to `1` when it is ready to process commands. **RDY** may be set to `1` before namespace(s) are ready to be accessed.

Setting this field from a `0` to a `1` when **RDY** is a `1`, or setting this field from a '1' to a '0' when **RDY** is a '0,' has undefined results. The Admin Queue registers (AQA, ASQ, and ACQ) will only be modified when **EN** is cleared to `0`.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.CSS

Specifies the I/O Command Set that is selected for use for the I/O Submission Queues.

Host software will only select a supported I/O Command Set, as indicated in the **CSS** field of [Controller Capabilities](ns-nvme-nvme_controller_capabilities.md).

This value of this field can only be changed when the controller is disabled ( the **EN** field is cleared to `0`). The selected I/O Command Set will be used for all I/O Submission Queues.

### -field DUMMYSTRUCTNAME.MPS

Indicates the host memory page size. The memory page size is `(2 ^ (12 + MPS))`. Thus, the minimum host memory page size is 4KB and the maximum host memory page size is 128MB.

The value set by host software must be a supported value as indicated by the **MPSMAX** and **MPSMIN** fields of [Controller Capabilities](ns-nvme-nvme_controller_capabilities.md). This field describes the value used for PRP entry size.

This field can only be modified when **EN** is cleared to `0`.

### -field DUMMYSTRUCTNAME.AMS

Specifies the arbitration mechanism to be used.

This field can only be modified when **EN** is cleared to `0`.

Host software can only set this field to supported arbitration mechanisms as indicated in the **AMS** field of [Controller Capabilities](ns-nvme-nvme_controller_capabilities.md). If this field is set to an unsupported value, the behavior is undefined.

### -field DUMMYSTRUCTNAME.SHN

Specifies a [NVME_CC_SHN_SHUTDOWN_NOTIFICATIONS](ne-nvme-nvme_cc_shn_shutdown_notifications.md) value that is used to initiate shutdown processing when a shutdown is occurring. For example, when a power down condition is expected.

For a normal shutdown notification, it is expected that the controller is given time to process the shutdown notification. For an abrupt shutdown notification, the host may not wait for shutdown processing to complete before power is lost. This field should be written to by host software prior to any power down condition and prior to any change of the PCI power management state. It is recommended that this field also be written to prior to a warm reboot. 

To determine when shutdown processing is complete, refer to the **SHST** value in [Controller Status](ns-nvme-nvme_controller_status.md).

### -field DUMMYSTRUCTNAME.IOSQES

Specifies the I/O Submission Queue entry size that is used for the selected I/O Command Set.

The required and maximum values for this field are specified in the **SQES.RequiredEntrySize** and **SQES.MaxEntrySize** fields of the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure for each I/O Command Set. The value is in bytes and is specified as a power of two (2^n).

### -field DUMMYSTRUCTNAME.IOCQES

Specifies the I/O Completion Queue entry size that is used for the selected I/O Command Set.

The required and maximum values for this field are specified in the **CQES.RequiredEntrySize** and **CQES.MaxEntrySize** fields of the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure for each I/O Command Set. The value is in bytes and is specified as a power of two (2^n).

### -field DUMMYSTRUCTNAME.Reserved1

### -field AsUlong

## -remarks

## -see-also

