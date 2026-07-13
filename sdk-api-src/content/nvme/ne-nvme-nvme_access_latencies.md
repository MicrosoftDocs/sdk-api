---
UID: NE:nvme.NVME_ACCESS_LATENCIES
tech.root: fs
title: NVME_ACCESS_LATENCIES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Defines values that indicate the latency of a read and write operation.
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
 - NVME_ACCESS_LATENCIES
f1_keywords:
 - NVME_ACCESS_LATENCIES
 - nvme/NVME_ACCESS_LATENCIES
dev_langs:
 - c++
---

# NVME_ACCESS_LATENCIES enumeration


## -description

Defines values that indicate the latency of a read and write operation.

## -enum-fields

### -field NVME_ACCESS_LATENCY_NONE

None. No latency information provided.

### -field NVME_ACCESS_LATENCY_IDLE

Idle. Longer latency acceptable.

### -field NVME_ACCESS_LATENCY_NORMAL

Normal. Typical latency.

### -field NVME_ACCESS_LATENCY_LOW

Low. Smallest possible latency.

## -remarks

This enumeration is used to specify values in the **AccessLatency** field of the [NVME_CDW13_READ_WRITE](ns-nvme-nvme_cdw13_read_write.md) structure and in the **AccessLatency** field of the [NVME_CONTEXT_ATTRIBUTES](ns-nvme-nvme_context_attributes.md) structure.

## -see-also

[NVME_CDW13_READ_WRITE struct](ns-nvme-nvme_cdw13_read_write.md)

