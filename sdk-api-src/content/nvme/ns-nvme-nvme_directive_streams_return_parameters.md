---
UID: NS:nvme.NVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS
tech.root: fs
title: NVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains return parameters for the Streams Directive.
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
req.typenames: NVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS, *PNVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS
 - NVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS
f1_keywords:
 - PNVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS
 - nvme/PNVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS
 - NVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS
 - nvme/NVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS
dev_langs:
 - c++
---

# NVME_DIRECTIVE_STREAMS_RETURN_PARAMETERS structure


## -description

Contains return parameters for the Streams Directive.

## -struct-fields

### -field MSL

The maximum streams limit.

### -field NSSA

The number of available NVM Subsystem streams.

### -field NSSO

The number of NVM Subsystem streams that are open.

### -field Reserved0

### -field SWS

The stream write size.

### -field SGS

The stream granularity size.

### -field NSA

The number of namespace streams that are allocated.

### -field NSO

The number of namespace streams that are open.

### -field Reserved1

## -remarks

## -see-also

