---
UID: NC:lpmapi.PFREEMEM
title: PFREEMEM
author: windows-sdk-content
description: The PFREEMEM function is a memory-freeing function provided by the PCM.
old-location: qos\pfreemem.htm
old-project: QOS
ms.assetid: b700b5c1-9fd7-4fc9-a5ed-f8ac75d22037
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: PFREEMEM, PFREEMEM callback, PFREEMEM callback function [QOS], _gqos_pfreemem, lpmapi/PFREEMEM, qos.pfreemem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: MC_TIMING_REPORT, *LPMC_TIMING_REPORT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Lpmapi.h
api_name:
 - PFREEMEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# PFREEMEM callback function


## -description


The 
<i>PFREEMEM</i> function is a memory-freeing function provided by the PCM. 
<i>PFREEMEM</i> frees memory buffers that were allocated using 
<a href="https://msdn.microsoft.com/e7b38820-4a7e-4f17-a67d-b94caa9037f5">PALLOCMEM</a>. The 
<i>PFREEMEM</i> function is supplied as a parameter of the 
<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a> function. The combination of 
<i>PALLOCMEM</i> and 
<i>PFREEMEM</i> allows the SBM to experiment with different memory-management schemes without requiring recompilation of LPMs.


## -parameters




### -param *pv [in]

Pointer to the memory buffer to free.


### -param *szFileName


### -param nLine








## -returns



This callback function does not return a value.




## -remarks



LPMs do not need to use this function to manage their local buffers. LPMs need to use this function to free buffers that were allocated, but were not sent to the PCM. For example, if a buffer is allocated in anticipation of a PCM's response to a request, but a response is never returned (perhaps the remote policy store is unavailable or unresponsive), that buffer must be freed with this function, or a memory leak will ensue.




## -see-also




<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a>



<a href="https://msdn.microsoft.com/e7b38820-4a7e-4f17-a67d-b94caa9037f5">PALLOCMEM</a>
 

 

