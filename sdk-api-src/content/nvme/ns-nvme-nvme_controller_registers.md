---
UID: NS:nvme.NVME_CONTROLLER_REGISTERS
tech.root: fs
title: NVME_CONTROLLER_REGISTERS
ms.date: 03/06/2025
ms.topic: language-reference
targetos: Windows
description: Specifies the register map for the controller.
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
req.typenames: NVME_CONTROLLER_REGISTERS, *PNVME_CONTROLLER_REGISTERS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CONTROLLER_REGISTERS
 - NVME_CONTROLLER_REGISTERS
f1_keywords:
 - PNVME_CONTROLLER_REGISTERS
 - nvme/PNVME_CONTROLLER_REGISTERS
 - NVME_CONTROLLER_REGISTERS
 - nvme/NVME_CONTROLLER_REGISTERS
dev_langs:
 - c++
---

# NVME_CONTROLLER_REGISTERS structure

## -description

Specifies the register map for the controller.

## -struct-fields

### -field CAP

A [NVME_CONTROLLER_CAPABILITIES](ns-nvme-nvme_controller_capabilities.md) structure that indicates the basic capabilities of the controller to host software.

The Controller Capabilities **CAP** register starts at Offset 00h.

### -field VS

a [NVME_VERSION](ns-nvme-nvme_version.md) structure that indicates the major and minor version of the NVM Express specification that the controller implementation supports. Valid versions of the specification are: 1.0, 1.1, and 1.2.

The Version **VS** register starts at Offset 08h.

### -field INTMS

Indicates whether an interrupt vector is masked from generating an interrupt or reporting a pending interrupt in the MSI Capability Structure.

When a value of `1` is written to a bit in the field, the corresponding interrupt vector is masked from generating an interrupt or reporting a pending interrupt in the MSI Capability Structure. Writing a `0` to a bit has no effect.

When read, this field returns the current interrupt mask value within the controller (not the value of this register). If a bit has a value of a `1`, the corresponding interrupt vector is masked. If a bit has a value of `0`, the corresponding interrupt vector is not masked.

This register is used to mask interrupts when using pin-based interrupts, single message MSI, or multiple message MSI. When using MSI-X, the interrupt mask table defined as part of MSI-X should be used to mask interrupts. Host software should not access this register when it is configured for MSI-X; any access when configured for MSI-X is undefined.

The Interrupt Mask Set **INTMS** register starts at Offset 0Ch.

### -field INTMC

Indicates whether an interrupt vector is masked.

When a value of `1` is written to a bit in the field, the corresponding interrupt vector is unmasked. Writing a `0` to a bit has no effect.

When read, this field returns the current interrupt mask value within the controller (not the value of this register). If a bit has a value of a `1`, then the corresponding interrupt vector is masked, If a bit has a value of `0`, then the corresponding interrupt vector is not masked.

This register is used to unmask interrupts when using pin-based interrupts, single message MSI, or multiple message MSI. When using MSI-X, the interrupt mask table defined as part of MSI-X should be used to unmask interrupts. Host software should not access this register when it is configured for MSI-X; any access when configured for MSI-X is undefined.

The Interrupt Mask Clear **INTMS** register starts at Offset 10h.

### -field CC

A [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md) structure that contains read/write configuration settings for the controller.

Host software must set the Arbitration Mechanism (**AMS**), Memory Page Size (**MPS**), and Command Set (**CSS**) fields in [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md) to valid values prior to enabling the controller by setting the Enable (**EN**) field to `1`.

The Controller Configuration **CC** register starts at Offset 14h.

### -field Reserved0

Offset 18h is reserved.

All reserved registers and all reserved bits within registers are read-only and return `0h` when read, however, software should not rely on `0h` being returned.

### -field CSTS

A [NVME_CONTROLLER_STATUS](ns-nvme-nvme_controller_status.md) structure that indicates controller status.

The Controller Status **CSTS** register starts at Offset 1Ch.

### -field NSSR

A [NVME_NVM_SUBSYSTEM_RESET](ns-nvme-nvme_nvm_subsystem_reset.md) structure that provides host software with the capability to initiate an NVM Subsystem Reset.

Support for this optional register is indicated by the state of the NVM Subsystem Reset Supported (**NSSRS**) field in the [Controller Capabilities](ns-nvme-nvme_controller_capabilities.md). If the register is not supported, then the address range occupied by the register is reserved.

The (Optional) NVM Subsystem Reset register starts at Offset 20h.

### -field AQA

A [NVME_ADMIN_QUEUE_ATTRIBUTES](ns-nvme-nvme_admin_queue_attributes.md) structure that specifies the Admin Queue Attributes for the Admin Submission Queue and Admin Completion Queue.

The Admin Queue Attributes **AQA** register starts at Offset 24h.

### -field ASQ

A [NVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS](ns-nvme-nvme_admin_submission_queue_base_address.md) structure that specifies the base memory address of the Admin Submission Queue.

The Admin Submission Queue Base Address register starts at Offset 28h.

### -field ACQ

A [NVME_ADMIN_COMPLETION_QUEUE_BASE_ADDRESS](ns-nvme-nvme_admin_completion_queue_base_address.md) structure that specifies the base memory address of the Admin Completion Queue.

Admin Completion Queue Base Address register starts at Offset 30h.

### -field CMBLOC

A [NVME_CONTROLLER_MEMORY_BUFFER_LOCATION](ns-nvme-nvme_controller_memory_buffer_location.md) structure that specifies the location of the Controller Memory Buffer.

If the value of **CMBSZ** is `0`, this register is reserved.

The (Optional) Controller Memory Buffer Location register starts at Offset 38h.

### -field CMBSZ

A [NVME_CONTROLLER_MEMORY_BUFFER_SIZE](ns-nvme-nvme_controller_memory_buffer_size.md) structure that specifies the size of the Controller Memory Buffer.

If the controller does not support the Controller Memory Buffer feature then this register is cleared to `0h`.

The (Optional) Controller Memory Buffer Size register starts at Offset 3Ch.

### -field Reserved2

Offset 40h to EFFh is reserved.

All reserved registers and all reserved bits within registers are read-only and return `0h` when read, however, software should not rely on `0h` being returned.

### -field Reserved3

Offset F00h to FFFh is reserved for Command Set specific registers.

All reserved registers and all reserved bits within registers are read-only and return `0h` when read, however, software should not rely on `0h` being returned.

### -field Doorbells

Specifies the start of the first Doorbell register. The Admin [Submission Queue Tail Doorbell](ns-nvme-nvme_submission_queue_tail_doorbell.md).

## -remarks

Controller registers are located in the Memory Register Lower Base Address (MLBAR)/Memory Register Upper Base Address (MUBAR) registers (PCI BAR0 and BAR1) that are mapped to a memory space that supports in-order access and variable access widths. For many computer architectures, specifying the memory space as uncacheable produces this behavior.

The host must not issue locked accesses, and must access registers in their native width or aligned 32-bit accesses. Violation of either of these host requirements results in undefined behavior.  

The Vendor Specific address range starts after the last doorbell supported by the controller and continues to the end of the BAR0/1 supported range. The start of the Vendor Specific address range starts at the same location and is not dependent on the number of allocated doorbells.

Accesses that target any portion of two or more registers are not supported.

## -see-also

- [NVME_ADMIN_QUEUE_ATTRIBUTES](ns-nvme-nvme_admin_queue_attributes.md)
- [NVME_ADMIN_COMPLETION_QUEUE_BASE_ADDRESS](ns-nvme-nvme_admin_completion_queue_base_address.md)
