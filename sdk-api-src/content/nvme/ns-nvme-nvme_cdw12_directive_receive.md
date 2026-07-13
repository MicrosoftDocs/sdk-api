---
UID: NS:nvme.NVME_CDW12_DIRECTIVE_RECEIVE
tech.root: fs
title: NVME_CDW12_DIRECTIVE_RECEIVE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains a parameter for allocating stream resources for the Directive Receive command.
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
req.typenames: NVME_CDW12_DIRECTIVE_RECEIVE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_CDW12_DIRECTIVE_RECEIVE
f1_keywords:
 - NVME_CDW12_DIRECTIVE_RECEIVE
 - nvme/NVME_CDW12_DIRECTIVE_RECEIVE
dev_langs:
 - c++
---

# NVME_CDW12_DIRECTIVE_RECEIVE structure


## -description

Contains a parameter for allocating stream resources for the Directive Receive command.

This structure is used as the value of the **CDW12** parameter in the **DIRECTIVERECEIVE** field of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field AllocateResources

A [NVME_CDW12_DIRECTIVE_RECEIVE_STREAMS_ALLOCATE_RESOURCES](ns-nvme-nvme_cdw12_directive_receive_streams_allocate_resources.md) structure that specifies the number of namespace streams requested.

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW10_DIRECTIVE_RECEIVE](ns-nvme-nvme_cdw10_directive_receive.md)
- [NVME_CDW11_DIRECTIVE_RECEIVE](ns-nvme-nvme_cdw11_directive_receive.md)

