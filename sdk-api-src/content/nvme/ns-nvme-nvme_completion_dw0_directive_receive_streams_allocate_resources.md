---
UID: NS:nvme.NVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
tech.root: fs
title: NVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains information about the number of allocated stream resources in a Directive Receive command.
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
req.typenames: NVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES, *PNVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
 - NVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
f1_keywords:
 - PNVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
 - nvme/PNVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
 - NVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
 - nvme/NVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
dev_langs:
 - c++
---

# NVME_COMPLETION_DW0_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES structure


## -description

Contains information about the number of allocated stream resources in a Directive Receive command.

This structure is posted to the Admin Completion Queue in the **DW0** field of the [NVME_COMPLETION_ENTRY](ns-nvme-nvme_completion_entry.md).

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.NSA

The number of allocated Namespace Streams.

### -field DUMMYSTRUCTNAME.Reserved

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCE](ns-nvme-nvme_cdw12_directive_receive_streams_allocate_resources.md)
- [NVME_CDW12_DIRECTIVE_RECEIVE](ns-nvme-nvme_cdw12_directive_receive.md)

