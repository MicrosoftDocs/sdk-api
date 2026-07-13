---
UID: NS:nvme.NVME_CDW11_IDENTIFY
tech.root: fs
title: NVME_CDW11_IDENTIFY
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains a parameter for the Identify command.
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
req.typenames: NVME_CDW11_IDENTIFY, *PNVME_CDW11_IDENTIFY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_IDENTIFY
 - NVME_CDW11_IDENTIFY
f1_keywords:
 - PNVME_CDW11_IDENTIFY
 - nvme/PNVME_CDW11_IDENTIFY
 - NVME_CDW11_IDENTIFY
 - nvme/NVME_CDW11_IDENTIFY
dev_langs:
 - c++
---

# NVME_CDW11_IDENTIFY structure


## -description

Contains a parameter for the Identify command.

The **NVME_CDW11_IDENTIFY** structure is used in the **CDW11** field of the **IDENTIFY** parameter in the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.NVMSETID

Specifies the NVM Set Identifier (NVMSETID) that is used as part of some Identify operations.

### -field DUMMYSTRUCTNAME.Reserved

### -field AsUlong

## -remarks

The Identify command returns information about the controller in the [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md) data structure, and namespace information in the [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md) data structure.

## -see-also

- [NVME_CDW10_IDENTIFY](ns-nvme-nvme_cdw10_identify.md)
- [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md)
- [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md)

