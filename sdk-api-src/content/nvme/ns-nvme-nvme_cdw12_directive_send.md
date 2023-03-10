---
UID: NS:nvme.NVME_CDW12_DIRECTIVE_SEND
tech.root: fs
title: NVME_CDW12_DIRECTIVE_SEND
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains a parameter for enabling a directive for the Directive Send command.
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
req.typenames: NVME_CDW12_DIRECTIVE_SEND
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_CDW12_DIRECTIVE_SEND
f1_keywords:
 - NVME_CDW12_DIRECTIVE_SEND
 - nvme/NVME_CDW12_DIRECTIVE_SEND
dev_langs:
 - c++
---

# NVME_CDW12_DIRECTIVE_SEND structure


## -description

Contains a parameter for enabling a directive for the Directive Send command.

This structure is used as the value of the **CDW12** parameter in the **DIRECTIVESEND** field of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field EnableDirective

A [NVME_CDW12_DIRECTIVE_SEND_IDENTIFY_ENABLE_DIRECTIVE](ns-nvme-nvme_cdw12_directive_send_identify_enable_directive.md) structure that specifies the directive type and whether it is enabled.

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW10_DIRECTIVE_SEND](ns-nvme-nvme_cdw10_directive_send.md)
- [NVME_CDW11_DIRECTIVE_SEND](ns-nvme-nvme_cdw11_directive_send.md)

