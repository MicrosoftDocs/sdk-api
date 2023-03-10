---
UID: NS:nvme.NVME_DIRECTIVE_STREAMS_GET_STATUS_DATA
tech.root: fs
title: NVME_DIRECTIVE_STREAMS_GET_STATUS_DATA
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains the identifiers of streams that are currently open.
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
req.typenames: NVME_DIRECTIVE_STREAMS_GET_STATUS_DATA, *PNVME_DIRECTIVE_STREAMS_GET_STATUS_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_DIRECTIVE_STREAMS_GET_STATUS_DATA
 - NVME_DIRECTIVE_STREAMS_GET_STATUS_DATA
f1_keywords:
 - PNVME_DIRECTIVE_STREAMS_GET_STATUS_DATA
 - nvme/PNVME_DIRECTIVE_STREAMS_GET_STATUS_DATA
 - NVME_DIRECTIVE_STREAMS_GET_STATUS_DATA
 - nvme/NVME_DIRECTIVE_STREAMS_GET_STATUS_DATA
dev_langs:
 - c++
---

# NVME_DIRECTIVE_STREAMS_GET_STATUS_DATA structure


## -description

Contains the identifiers of streams that are currently open.

## -struct-fields

### -field OpenStreamCount

The number of currently open streams.

### -field StreamIdentifiers

An array of stream IDs that indicate which streams are currently open.

The array is of size **NVME_STREAMS_GET_STATUS_MAX_IDS**.

## -remarks

## -see-also

