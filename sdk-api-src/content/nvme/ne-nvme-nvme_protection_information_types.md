---
UID: NE:nvme.NVME_PROTECTION_INFORMATION_TYPES
tech.root: fs
title: NVME_PROTECTION_INFORMATION_TYPES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate whether end-to-end data protection is enabled, and if it is, specifies the type of protection information.
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
 - NVME_PROTECTION_INFORMATION_TYPES
f1_keywords:
 - NVME_PROTECTION_INFORMATION_TYPES
 - nvme/NVME_PROTECTION_INFORMATION_TYPES
dev_langs:
 - c++
---

# NVME_PROTECTION_INFORMATION_TYPES enumeration


## -description

Contains values that indicate whether end-to-end data protection is enabled, and if it is, specifies the type of protection information.

When end-to-end data protection is enabled, the host must specify the appropriate protection information in the Read, Write, or Compare commands.

## -enum-fields

### -field NVME_PROTECTION_INFORMATION_NOT_ENABLED

Protection information is not enabled.

### -field NVME_PROTECTION_INFORMATION_TYPE1

Type 1 protection information is enabled.

### -field NVME_PROTECTION_INFORMATION_TYPE2

Type 2 protection information is enabled.

### -field NVME_PROTECTION_INFORMATION_TYPE3

Type 3 protection information is enabled.

## -remarks

Use this enumeration to specify values in the **PI** field of the [NVME_CDW10_FORMAT_NVM](ns-nvme-nvme_cdw10_format_nvm.md) structure that is used in the [FORMAT NVM (FORMATNVM)](ns-nvme-nvme_command.md) Admin command.

## -see-also

- [NVME_CDW10_FORMAT_NVM](ns-nvme-nvme_cdw10_format_nvm.md)

