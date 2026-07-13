---
UID: NS:nvme.NVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE
tech.root: fs
title: NVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for specifying and enabling directives in the Directive Send command.
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
req.typenames: NVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE, *PNVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE
 - NVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE
f1_keywords:
 - PNVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE
 - nvme/PNVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE
 - NVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE
 - nvme/NVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE
dev_langs:
 - c++
---

# NVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE structure


## -description

Contains parameters for specifying and enabling directives in the Directive Send command.

This structure is used as the value of the **EnableDirective** field in the [NVME_CDW12_DIRECTIVE_SEND](ns-nvme-nvme_cdw12_directive_send.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.ENDIR

Specifies whether the directive is enabled.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.DTYPE

Specifies the directive type.

### -field DUMMYSTRUCTNAME.Reserved1

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW12_DIRECTIVE_SEND](ns-nvme-nvme_cdw12_directive_send.md)

