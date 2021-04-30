---
UID: NC:lpmapi.PALLOCMEM
title: PALLOCMEM (lpmapi.h)
description: The PALLOCMEM function is a memory allocation function provided by the PCM, used for allocating memory when returning policy information to the PCM.
helpviewer_keywords: ["PALLOCMEM","PALLOCMEM callback","PALLOCMEM callback function [QOS]","_gqos_pallocmem","lpmapi/PALLOCMEM","qos.pallocmem"]
old-location: qos\pallocmem.htm
tech.root: QOS
ms.assetid: e7b38820-4a7e-4f17-a67d-b94caa9037f5
ms.date: 12/05/2018
ms.keywords: PALLOCMEM, PALLOCMEM callback, PALLOCMEM callback function [QOS], _gqos_pallocmem, lpmapi/PALLOCMEM, qos.pallocmem
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PALLOCMEM
 - lpmapi/PALLOCMEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Lpmapi.h
api_name:
 - PALLOCMEM
---

# PALLOCMEM callback function


## -description

The 
<i>PALLOCMEM</i> function is a memory allocation function provided by the PCM, used for allocating memory when returning policy information to the PCM. The 
<i>PALLOCMEM</i> function is supplied as a parameter of the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a> function, and allows the SBM to experiment with different memory-management schemes without requiring recompilation of LPMs.

## -parameters

### -param Size [in]

Size of the memory buffer required by the LPM.

### -param szFileName

### -param nLine

## -returns

Returns a pointer to the requested memory allocation.

## -remarks

LPMs do not need to use this function to manage their local buffers.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a>
