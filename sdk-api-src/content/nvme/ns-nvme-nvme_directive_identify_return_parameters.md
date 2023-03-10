---
UID: NS:nvme.NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS
tech.root: fs
title: NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains fields that describe return parameters for the Identify Directive.
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
req.typenames: NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS, *PNVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS
 - NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS
f1_keywords:
 - PNVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS
 - nvme/PNVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS
 - NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS
 - nvme/NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS
dev_langs:
 - c++
---

# NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS structure


## -description

Contains fields that describe return parameters for the Identify Directive.

## -struct-fields

### -field DirectivesSupported

A [NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR](ns-nvme-nvme_directive_identify_return_parameters_descriptor.md) structure containing values that indicate which directives are supported.

### -field DirectivesEnabled

A [NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR](ns-nvme-nvme_directive_identify_return_parameters_descriptor.md) structure containing values that indicate which directives are enabled.

## -remarks

This data structure is 4KB in size.

## -see-also

- [NVME_DIRECTIVE_IDENTIFY_RETURN_PARAMETERS_DESCRIPTOR](ns-nvme-nvme_directive_identify_return_parameters_descriptor.md)

