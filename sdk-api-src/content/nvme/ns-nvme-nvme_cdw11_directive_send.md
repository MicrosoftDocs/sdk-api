---
UID: NS:nvme.__unnamed_union_127
tech.root: fs 
title: NVME_CDW11_DIRECTIVE_SEND
ms.date: 02/19/2021 
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Directive Send command.
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
req.typenames: NVME_CDW11_DIRECTIVE_SEND, *PNVME_CDW11_DIRECTIVE_SEND
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_DIRECTIVE_SEND
 - NVME_CDW11_DIRECTIVE_SEND
f1_keywords:
 - PNVME_CDW11_DIRECTIVE_SEND
 - nvme/PNVME_CDW11_DIRECTIVE_SEND
 - NVME_CDW11_DIRECTIVE_SEND
 - nvme/NVME_CDW11_DIRECTIVE_SEND
dev_langs:
 - c++
---

# NVME_CDW11_DIRECTIVE_SEND structure

## -description

Contains parameters for the Directive Send command.

This structure is used as the value of the **CDW11** parameter in the **DIRECTIVESEND** field of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.DOPER

The directive operation.

### -field DUMMYSTRUCTNAME.DTYPE

The directive type.

### -field DUMMYSTRUCTNAME.DSPEC

A directive specific value.

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW10_DIRECTIVE_SEND](ns-nvme-nvme_cdw10_dataset_management.md)