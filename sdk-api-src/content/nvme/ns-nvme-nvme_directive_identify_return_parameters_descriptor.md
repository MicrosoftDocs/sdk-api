---
UID: NS:nvme.NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR
tech.root: fs
title: NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that describe return parameters for the Identify Directive.
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
req.typenames: NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR, *PNVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR
 - NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR
f1_keywords:
 - PNVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR
 - nvme/PNVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR
 - NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR
 - nvme/NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR
dev_langs:
 - c++
---

# NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR structure


## -description

Contains values that describe return parameters for the Identify Directive.

This structure is used in the **DirectivesSupported** and **DirectivesEnabled** parameters of the [NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS](ns-nvme-nvme_directive_identify_return_parameters.md) structure.

## -struct-fields

### -field Identify

The return parameter is an [NVME_DIRECTIVE_TYPE_IDENTIFY](ne-nvme-nvme_directive_types.md), a directive for an Identify operation.

### -field Streams

The return parameter is an [NVME_DIRECTIVE_TYPE_STREAMS](ne-nvme-nvme_directive_types.md), a directive for a Streams operation.

### -field Reserved0

### -field Reserved1

## -remarks

## -see-also

- [NVME_DIRECTIVE_TYPES](ne-nvme-nvme_directive_types.md)
- [NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS](ns-nvme-nvme_directive_identify_return_parameters.md)

