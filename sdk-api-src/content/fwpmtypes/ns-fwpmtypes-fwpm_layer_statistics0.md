---
UID: NS:fwpmtypes.FWPM_LAYER_STATISTICS0_
title: FWPM_LAYER_STATISTICS0 (fwpmtypes.h)
description: Stores statistics related to a layer.
helpviewer_keywords: ["FWPM_LAYER_STATISTICS0","FWPM_LAYER_STATISTICS0 structure [Filtering]","fwp.fwpm_layer_statistics0","fwpmtypes/FWPM_LAYER_STATISTICS0"]
old-location: fwp\fwpm_layer_statistics0.htm
tech.root: fwp
ms.assetid: cc8e0159-fe28-4718-b5fe-d38d180b3e2c
ms.date: 12/05/2018
ms.keywords: FWPM_LAYER_STATISTICS0, FWPM_LAYER_STATISTICS0 structure [Filtering], fwp.fwpm_layer_statistics0, fwpmtypes/FWPM_LAYER_STATISTICS0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_LAYER_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_LAYER_STATISTICS0_
 - fwpmtypes/FWPM_LAYER_STATISTICS0_
 - FWPM_LAYER_STATISTICS0
 - fwpmtypes/FWPM_LAYER_STATISTICS0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_LAYER_STATISTICS0
---

# FWPM_LAYER_STATISTICS0 structure


## -description

The <b>FWPM_LAYER_STATISTICS0</b> structure stores statistics related to a layer.

## -struct-fields

### -field layerId

Type: <b>GUID</b>

Identifier of the layer.

### -field classifyPermitCount

Type: <b>UINT32</b>

Number of permitted connections.

### -field classifyBlockCount

Type: <b>UINT32</b>

Number of blocked connections.

### -field classifyVetoCount

Type: <b>UINT32</b>

Number of vetoed connections.

### -field numCacheEntries

Type: <b>UINT32</b>

## -remarks

<b>FWPM_LAYER_STATISTICS0</b> is a specific implementation of FWPM_LAYER_STATISTICS. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_STATISTICS0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_statistics0)