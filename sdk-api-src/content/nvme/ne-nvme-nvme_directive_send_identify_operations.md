---
UID: NE:nvme.NVME_DIRECTIVE_SEND_IDENTIFY_OPERATIONS
tech.root: fs
title: NVME_DIRECTIVE_SEND_IDENTIFY_OPERATIONS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains a value that specifies a directive type sent to an Identify operation.
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
 - NVME_DIRECTIVE_SEND_IDENTIFY_OPERATIONS
f1_keywords:
 - NVME_DIRECTIVE_SEND_IDENTIFY_OPERATIONS
 - nvme/NVME_DIRECTIVE_SEND_IDENTIFY_OPERATIONS
dev_langs:
 - c++
---

# NVME_DIRECTIVE_SEND_IDENTIFY_OPERATIONS enumeration


## -description

Contains a value that specifies a directive type sent to an Identify operation.

## -enum-fields

### -field NVME_DIRECTIVE_SEND_IDENTIFY_OPERATION_ENABLE_DIRECTIVE

Indicates whether to send an enable directive to an Identify operation.

## -remarks

Use this enumeration to specify values in the **DTYPE** member of the [NVME_CDW11_DIRECTIVE_SEND](ns-nvme-nvme_cdw11_directive_send.md) structure.

## -see-also

[NVME_CDW11_DIRECTIVE_SEND](ns-nvme-nvme_cdw11_directive_send.md)

