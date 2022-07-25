---
UID: NC:lpmapi.PFREEMEM
title: PFREEMEM (lpmapi.h)
description: The PFREEMEM function is a memory-freeing function provided by the PCM.
helpviewer_keywords: ["PFREEMEM","PFREEMEM callback","PFREEMEM callback function [QOS]","_gqos_pfreemem","lpmapi/PFREEMEM","qos.pfreemem"]
old-location: qos\pfreemem.htm
tech.root: QOS
ms.assetid: b700b5c1-9fd7-4fc9-a5ed-f8ac75d22037
ms.date: 12/05/2018
ms.keywords: PFREEMEM, PFREEMEM callback, PFREEMEM callback function [QOS], _gqos_pfreemem, lpmapi/PFREEMEM, qos.pfreemem
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
 - PFREEMEM
 - lpmapi/PFREEMEM
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
 - PFREEMEM
---

# PFREEMEM callback function


## -description

The 
<i>PFREEMEM</i> function is a memory-freeing function provided by the PCM. 
<i>PFREEMEM</i> frees memory buffers that were allocated using 
<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-pallocmem">PALLOCMEM</a>. The 
<i>PFREEMEM</i> function is supplied as a parameter of the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a> function. The combination of 
<i>PALLOCMEM</i> and 
<i>PFREEMEM</i> allows the SBM to experiment with different memory-management schemes without requiring recompilation of LPMs.

## -parameters

### -param pv [in]

Pointer to the memory buffer to free.

### -param szFileName

### -param nLine

## -remarks

LPMs do not need to use this function to manage their local buffers. LPMs need to use this function to free buffers that were allocated, but were not sent to the PCM. For example, if a buffer is allocated in anticipation of a PCM's response to a request, but a response is never returned (perhaps the remote policy store is unavailable or unresponsive), that buffer must be freed with this function, or a memory leak will ensue.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-pallocmem">PALLOCMEM</a>
