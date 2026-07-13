---
UID: NS:nvme.NVME_CONTROLLER_MEMORY_BUFFER_SIZE
tech.root: fs
title: NVME_CONTROLLER_MEMORY_BUFFER_SIZE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Defines the size of the optional Controller Memory Buffer register, and is used in the **CMBSZ** field of the [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md) structure.
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
req.typenames: NVME_CONTROLLER_MEMORY_BUFFER_SIZE, *PNVME_CONTROLLER_MEMORY_BUFFER_SIZE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CONTROLLER_MEMORY_BUFFER_SIZE
 - NVME_CONTROLLER_MEMORY_BUFFER_SIZE
f1_keywords:
 - PNVME_CONTROLLER_MEMORY_BUFFER_SIZE
 - nvme/PNVME_CONTROLLER_MEMORY_BUFFER_SIZE
 - NVME_CONTROLLER_MEMORY_BUFFER_SIZE
 - nvme/NVME_CONTROLLER_MEMORY_BUFFER_SIZE
dev_langs:
 - c++
---

# NVME_CONTROLLER_MEMORY_BUFFER_SIZE structure


## -description

Defines the size of the optional Controller Memory Buffer register, and is used in the **CMBSZ** field of the [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md) structure.

If the controller does not support the Controller Memory Buffer feature, the **CMBSZ** field is cleared to `0h`.

The location of the Controller Memory Buffer is specified in the **CMBLOC** field of **NVME_CONTROLLER_REGISTERS**.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.SQS

Indicates whether the controller supports Admin and I/O Submission Queues in the Controller Memory Buffer.

When this value is set to `1`, the controller supports Admin and I/O Submission Queues in the Controller Memory Buffer. 
When this value is cleared to `0`, all Submission Queues will be placed in host memory.

### -field DUMMYSTRUCTNAME.CQS

Indicates whether the controller supports Admin and I/O Completion Queues in the Controller Memory Buffer.

When this value is set to `1`, the controller supports Admin and I/O Completion Queues in the Controller Memory Buffer. 
When this value is cleared to `0`, all Completion Queues will be placed in host memory.

### -field DUMMYSTRUCTNAME.LISTS

Indicates whether the controller supports Physical Region Page (PRP) and Scatter Gather Lists (SGL) in the Controller Memory Buffer.

When this value is set to `1`, the controller supports PRP Lists in the Controller Memory Buffer. If the value is set to `1` and SGLs are supported by the controller, the controller supports SGLs in the Controller Memory Buffer. If this bit is set to `1`, the Submission Queue Support (**SQS**) field will be set to `1`.

When this value is cleared to `0`, all PRP Lists and SGLs will be placed in host memory.

### -field DUMMYSTRUCTNAME.RDS

Indicates whether the controller supports data and metadata in the Controller Memory Buffer for commands, such as the Read command, that transfer data from the controller to the host.

When this value is set to `1`, the controller supports data and metadata in the Controller Memory Buffer for commands that transfer data from the controller to the host.

When this value is cleared to `0`, all data and metadata for commands that transfer data from the controller to the host will be transferred to host memory.

### -field DUMMYSTRUCTNAME.WDS

Indicates whether the controller supports data and metadata in the Controller Memory Buffer for commands, such as the Write command, that transfer data from the host to the controller.

When this value is set to `1`, the controller supports data and metadata in the Controller Memory Buffer for commands that transfer data from the host to the controller.

When this value is cleared to `0`, all data and metadata for commands that transfer data from the host to the controller will be transferred from host memory.

### -field DUMMYSTRUCTNAME.Reserved

### -field DUMMYSTRUCTNAME.SZU

A [NVME_CMBSZ_SIZE_UNITS](ne-nvme-nvme_cmbsz_size_units.md) value that indicates the granularity of the Size **SZ** field.

### -field DUMMYSTRUCTNAME.SZ

Indicates the size of the Controller Memory Buffer available for use by the host. The size is in multiples of the Size Unit **SZU**.

If the Offset (the **OFST** field in the [NVME_CONTROLLER_MEMORY_BUFFER_LOCATION](ns-nvme-nvme_controller_memory_buffer_location.md) structure) + Size (**SZ**) exceeds the length of the specified Base Address Register (the **BIR** field in the [NVME_CONTROLLER_MEMORY_BUFFER_LOCATION](ns-nvme-nvme_controller_memory_buffer_location.md) structure), the size available to the host is limited by the length of the Base Address Register.

### -field AsUlong

## -remarks

## -see-also

- [NVME_CONTROLLER_MEMORY_BUFFER_LOCATION](ns-nvme-nvme_controller_memory_buffer_location.md)

