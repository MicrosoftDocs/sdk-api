---
UID: NE:nvme.NVME_DIRECTIVE_SEND_STREAMS_OPERATIONS
tech.root: fs
title: NVME_DIRECTIVE_SEND_STREAMS_OPERATIONS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate a directive type sent to a Streams operation.
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
 - NVME_DIRECTIVE_SEND_STREAMS_OPERATIONS
f1_keywords:
 - NVME_DIRECTIVE_SEND_STREAMS_OPERATIONS
 - nvme/NVME_DIRECTIVE_SEND_STREAMS_OPERATIONS
dev_langs:
 - c++
---

# NVME_DIRECTIVE_SEND_STREAMS_OPERATIONS enumeration


## -description

Contains values that indicate a directive type sent to a Streams operation.

## -enum-fields

### -field NVME_DIRECTIVE_SEND_STREAMS_OPERATION_RELEASE_IDENTIFIER

A release identifier directive sent to a Streams operation.

### -field NVME_DIRECTIVE_SEND_STREAMS_OPERATION_RELEASE_RESOURCES

A release resources directive sent to a Streams operation.

## -remarks

Use this enumeration to specify values in the **DTYPE** member of the [NVME_CDW11_DIRECTIVE_SEND](ns-nvme-nvme_cdw11_directive_send.md) structure.

## -see-also

[NVME_CDW11_DIRECTIVE_SEND](ns-nvme-nvme_cdw11_directive_send.md)

