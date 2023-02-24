---
UID: NS:nvme.NVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
tech.root: fs
title: NVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains a parameter for requesting namespace streams that is used for allocating stream resources in the Directive Receive command.
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
req.typenames: NVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES, *PNVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
 - NVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
f1_keywords:
 - PNVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
 - nvme/PNVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
 - NVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
 - nvme/NVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES
dev_langs:
 - c++
---

# NVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES structure


## -description

Contains a parameter for requesting namespace streams that is used for allocating stream resources in the Directive Receive command.

This structure is used as the value of the **AllocateResources** field in the [NVME_CDW12_DIRECTIVE_RECEIVE](ns-nvme-nvme_cdw12_directive_receive.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.NSR

Specifies the number of namespace streams requested.

### -field DUMMYSTRUCTNAME.Reserved

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW12_DIRECTIVE_RECEIVE](ns-nvme-nvme_cdw12_directive_receive.md)

