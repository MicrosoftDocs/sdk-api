---
UID: NS:nvme.NVME_CDW10_IDENTIFY
tech.root: fs
title: NVME_CDW10_IDENTIFY
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Identify command that returns a data buffer that describes information about the NVM subsystem, the controller or the namespace(s).
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
req.typenames: NVME_CDW10_IDENTIFY, *PNVME_CDW10_IDENTIFY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_IDENTIFY
 - NVME_CDW10_IDENTIFY
f1_keywords:
 - PNVME_CDW10_IDENTIFY
 - nvme/PNVME_CDW10_IDENTIFY
 - NVME_CDW10_IDENTIFY
 - nvme/NVME_CDW10_IDENTIFY
dev_langs:
 - c++
---

# NVME_CDW10_IDENTIFY structure


## -description

Contains parameters for the Identify command that returns a data buffer that describes information about the NVM subsystem, the controller or the namespace(s).

The **NVME_CDW10_IDENTIFY** structure is used in the **CDW10** field of the **IDENTIFY** parameter in the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.CNS

Specifies an [NVME_IDENTIFY_CNS_CODES](ne-nvme-nvme_identify_cns_codes.md) value that indicates the information to be returned to the host.

### -field DUMMYSTRUCTNAME.Reserved

### -field DUMMYSTRUCTNAME.CNTID

Specifies the Controller Identifier (CNTID) that is used as part of some Identify operations.

If this field is not used as part of the Identify operation, then host software will clear this field to `0h`. Controllers that support Namespace Management should support this field.

### -field AsUlong

## -remarks

The Identify command returns information about the controller in the [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md) data structure, and namespace information in the [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md) data structure.

## -see-also

- [NVME_CDW11_IDENTIFY](ns-nvme-nvme_cdw11_identify.md)
- [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md)
- [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md)

