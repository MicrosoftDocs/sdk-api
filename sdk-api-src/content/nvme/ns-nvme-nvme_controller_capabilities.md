---
UID: NS:nvme.NVME_CONTROLLER_CAPABILITIES
tech.root: fs
title: NVME_CONTROLLER_CAPABILITIES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains read only values that specify the basic capabilities of the controller to host software.
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
req.typenames: NVME_CONTROLLER_CAPABILITIES, *PNVME_CONTROLLER_CAPABILITIES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CONTROLLER_CAPABILITIES
 - NVME_CONTROLLER_CAPABILITIES
f1_keywords:
 - PNVME_CONTROLLER_CAPABILITIES
 - nvme/PNVME_CONTROLLER_CAPABILITIES
 - NVME_CONTROLLER_CAPABILITIES
 - nvme/NVME_CONTROLLER_CAPABILITIES
dev_langs:
 - c++
---

# NVME_CONTROLLER_CAPABILITIES structure


## -description

Contains read only values that specify the basic capabilities of the controller to host software.

This structure is used in the Controller Capabilities (**CAP**) field of the [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.MQES

Indicates the maximum individual queue size that the controller supports.

This value applies to each of the I/O Submission Queues and I/O Completion Queues that the host software creates.

This is a 0’s based value. The minimum value is `1h`, indicating two queue entries.

### -field DUMMYSTRUCTNAME.CQR

Indicates whether I/O Submission Queues and I/O Completion Queues are required by the controller to be physically contiguous.

When this field is set to `1`, the controller requires that I/O Submission Queues and I/O Completion Queues are physically contiguous.
When this field is cleared to `0`, the controller supports I/O Submission Queues and I/O Completion Queues that are not physically contiguous.

When this field is set to `1`, the Physically Contiguous bit (the **PC** field) in the [Create I/O Submission Queue](ns-nvme-nvme_cdw11_create_io_sq.md) and [Create I/O Completion Queue](ns-nvme-nvme_cdw11_create_io_cq.md) commands is set to `1`.

### -field DUMMYSTRUCTNAME.AMS_WeightedRoundRobinWithUrgent

Indicates whether the Weighted Round Robin with Urgent Priority Class arbitration mechanism is supported by the controller.

When this field is set to `1`, the Weighted Round Robin with Urgent Priority Class arbitration mechanism is supported.

This **AMS_WeightedRoundRobinWithUrgent** and **AMS_VendorSpecific** fields indicate the optional arbitration mechanisms supported by the controller. The round robin arbitration mechanism is not listed since all controllers must support this arbitration mechanism.

### -field DUMMYSTRUCTNAME.AMS_VendorSpecific

Indicates whether the Vendor Specific arbitration mechanism is supported by the controller.

When this field is set to `1`, the Vendor Specific arbitration mechanism is supported.

### -field DUMMYSTRUCTNAME.Reserved0

A reserved field (bits 19 to 23).

### -field DUMMYSTRUCTNAME.TO

Indicates the worst case time that the host software will wait for the Ready (**RDY**) value in [Controller Status](ns-nvme-nvme_controller_status.md) to transition from:

- `0` to `1` after the **EN** value in [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md) transitions from `0` to `1`; or
- `1` to `0` after the **EN** value in [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md) transitions from `1` to `0`.

This worst case time may be experienced after events such as an abrupt shutdown or activation of a new firmware image. Typical times are expected to be much shorter.

The value of this field is in 500 millisecond units.

### -field DUMMYSTRUCTNAME.DSTRD

Indicates the *stride* between doorbell registers.

Each [Submission Queue](ns-nvme-nvme_submission_queue_tail_doorbell.md) and [Completion Queue](ns-nvme-nvme_completion_queue_head_doorbell.md) Doorbell register is 32-bits in size. The stride is specified as `(2 ^ (2 + DSTRD))` in bytes.

A value of `0h` indicates a stride of 4 bytes, where the doorbell registers are packed without reserved space between each register.

### -field DUMMYSTRUCTNAME.NSSRS

Indicates whether the controller supports the NVM Subsystem Reset feature defined in the [NVME_NVM_SUBSYSTEM_RESET](ns-nvme-nvme_nvm_subsystem_reset.md) structure.

When this field is set to `1`, the controller supports the NVM Subsystem Reset feature.
hen this field is cleared to `0`, the controller does not support the NVM Subsystem Reset feature.

### -field DUMMYSTRUCTNAME.CSS_NVM

This field indicates whether the NVM Command Set is supported by the controller. A minimum of one command set must be supported.

When this field is set to `1`, the NVM Command Set is supported.

The **CSS_Reserved0** through **CSS_Reserved6** fields are reserved for other I/O Command Sets, if the value of one of these fields is set to `1`, then the corresponding I/O Command Set is supported.

### -field DUMMYSTRUCTNAME.CSS_Reserved0

### -field DUMMYSTRUCTNAME.CSS_Reserved1

### -field DUMMYSTRUCTNAME.CSS_Reserved2

### -field DUMMYSTRUCTNAME.CSS_Reserved3

### -field DUMMYSTRUCTNAME.CSS_Reserved4

### -field DUMMYSTRUCTNAME.CSS_Reserved5

### -field DUMMYSTRUCTNAME.CSS_Reserved6

### -field DUMMYSTRUCTNAME.Reserved2

### -field DUMMYSTRUCTNAME.MPSMIN

Indicates the minimum host memory page size that the controller supports.

The minimum memory page size is `(2 ^ (12 + MPSMIN))`.

The host will not configure a memory page size in the **MPS** field of [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md) that is smaller than this value.

### -field DUMMYSTRUCTNAME.MPSMAX

Indicates the maximum host memory page size that the controller supports.

The maximum memory page size is `(2 ^ (12 + MPSMAX))`.

The host will not configure a memory page size in the **MPS** field of [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md) that is larger than this value.

### -field DUMMYSTRUCTNAME.Reserved3

### -field AsUlonglong

## -remarks

## -see-also

- [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md)
- [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md)

