---
UID: NS:nvme._NVME_NVM_SUBSYSTEM_RESET
tech.root: fs 
title: NVME_NVM_SUBSYSTEM_RESET
ms.date: 02/19/2021 
ms.topic: language-reference
targetos: Windows
description: Specifies a parameter that provides host software with the capability to initiate an NVM Subsystem Reset.
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
req.typenames: NVME_NVM_SUBSYSTEM_RESET, *PNVME_NVM_SUBSYSTEM_RESET
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - _NVME_NVM_SUBSYSTEM_RESET
 - PNVME_NVM_SUBSYSTEM_RESET
 - NVME_NVM_SUBSYSTEM_RESET
f1_keywords:
 - _NVME_NVM_SUBSYSTEM_RESET
 - nvme/_NVME_NVM_SUBSYSTEM_RESET
 - PNVME_NVM_SUBSYSTEM_RESET
 - nvme/PNVME_NVM_SUBSYSTEM_RESET
 - NVME_NVM_SUBSYSTEM_RESET
 - nvme/NVME_NVM_SUBSYSTEM_RESET
dev_langs:
 - c++
---

# NVME_NVM_SUBSYSTEM_RESET structure

## -description

Specifies a parameter that provides host software with the capability to initiate an NVM Subsystem Reset.

This structure is used in the **NSSR** field of the [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md) structure.

## -struct-fields

### -field NSSRC

A read/write value that initiates an NVM Subsystem Reset.

Writing the value `4E564D65h` ("NVMe") to this field initiates an NVM Subsystem Reset. Writing any other value has no functional effect on the operation of the NVM subsystem.

This field returns the value `0h` when read.

## -remarks

## -see-also

