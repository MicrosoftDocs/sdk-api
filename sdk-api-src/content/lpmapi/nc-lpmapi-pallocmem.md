---
UID: NC:lpmapi.PALLOCMEM
title: PALLOCMEM
author: windows-driver-content
description: The PALLOCMEM function is a memory allocation function provided by the PCM, used for allocating memory when returning policy information to the PCM.
old-location: qos\pallocmem.htm
old-project: QOS
ms.assetid: e7b38820-4a7e-4f17-a67d-b94caa9037f5
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: PALLOCMEM, PALLOCMEM callback function [QOS], _gqos_pallocmem, lpmapi/PALLOCMEM, qos.pallocmem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MC_TIMING_REPORT, *LPMC_TIMING_REPORT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Lpmapi.h
api_name:
-	PALLOCMEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# PALLOCMEM callback


## -description


The 
<i>PALLOCMEM</i> function is a memory allocation function provided by the PCM, used for allocating memory when returning policy information to the PCM. The 
<i>PALLOCMEM</i> function is supplied as a parameter of the 
<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a> function, and allows the SBM to experiment with different memory-management schemes without requiring recompilation of LPMs.


## -parameters




### -param Size [in]

Size of the memory buffer required by the LPM.


### -param *szFileName


### -param nLine








## -returns



Returns a pointer to the requested memory allocation.




## -remarks



LPMs do not need to use this function to manage their local buffers.




## -see-also




<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a>
 

 

