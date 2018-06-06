---
UID: NC:ras.PFNRASFREEBUFFER
title: PFNRASFREEBUFFER
author: windows-sdk-content
description: The custom-scripting DLL calls RasFreeBuffer to release a memory buffer that was allocated by a previous call to RasGetBuffer.
old-location: rras\rasfreebuffer.htm
old-project: RRAS
ms.assetid: aba43ef9-7f62-48ab-a790-c8592a57f2c2
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: PFNRASFREEBUFFER, PFNRASFREEBUFFER callback, RasFreeBuffer, RasFreeBuffer callback function [RAS], _ras_rasfreebuffer, ras/RasFreeBuffer, rras.rasfreebuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ras.h
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
req.typenames: RSVP_STATUS_INFO, *LPRSVP_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasFreeBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PFNRASFREEBUFFER callback function


## -description


The custom-scripting DLL calls 
<i>RasFreeBuffer</i> to release a memory buffer that was allocated by a previous call to 
<a href="https://msdn.microsoft.com/655f2dfa-a6cf-43db-8d2e-bf9a10163c75">RasGetBuffer</a>. 


## -parameters




### -param pBufer








#### - pBuffer

Pointer to the memory buffer to free. This memory must have been obtained by a previous call to 
<a href="https://msdn.microsoft.com/655f2dfa-a6cf-43db-8d2e-bf9a10163c75">RasGetBuffer</a>.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The pointer to the buffer passed in the <i>pBuffer</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PORT_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>hPort</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



The custom-scripting DLL calls 
<i>RasFreeBuffer</i> through a function pointer. The function pointer is passed to the custom-scripting DLL as a parameter when RAS calls the DLL's implementation of 
<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>.




## -see-also




<a href="https://msdn.microsoft.com/c27b8b02-6018-4441-a355-1fb890b9001c">RAS Custom-Scripting</a>



<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>



<a href="https://msdn.microsoft.com/655f2dfa-a6cf-43db-8d2e-bf9a10163c75">RasGetBuffer</a>
 

 

