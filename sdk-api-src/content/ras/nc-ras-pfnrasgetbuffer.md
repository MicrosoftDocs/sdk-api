---
UID: NC:ras.PFNRASGETBUFFER
title: PFNRASGETBUFFER
author: windows-sdk-content
description: The custom-scripting DLL calls RasGetBuffer to allocate memory for sending or receiving data over the port connected to the server.
old-location: rras\rasgetbuffer.htm
old-project: rras
ms.assetid: 655f2dfa-a6cf-43db-8d2e-bf9a10163c75
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PFNRASGETBUFFER, PFNRASGETBUFFER callback, RasGetBuffer, RasGetBuffer callback function [RAS], _ras_rasgetbuffer, ras/RasGetBuffer, rras.rasgetbuffer
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
 - RasGetBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PFNRASGETBUFFER callback function


## -description


The custom-scripting DLL calls 
<i>RasGetBuffer</i> to allocate memory for sending or receiving data over the port connected to the server. 
		


## -parameters




### -param *ppBuffer

Pointer to a pointer that receives the address of the returned buffer.


### -param pdwSize

Pointer to a <b>DWORD</b> variable that, on input, contains the requested size of the buffer. On output, this variable contains the actual size of the buffer allocated.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is the following error code.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUT_OF_BUFFERS</b></dt>
</dl>
</td>
<td width="60%">
RAS cannot allocate anymore buffer space.

</td>
</tr>
</table>
 




## -remarks



The maximum buffer size that can be obtained is 1500 bytes.

The custom-scripting DLL calls 
<i>RasGetBuffer</i> through a function pointer. The function pointer is passed to the custom-scripting DLL as a parameter when RAS calls the DLL's implementation of 
<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>.




## -see-also




<a href="https://msdn.microsoft.com/c27b8b02-6018-4441-a355-1fb890b9001c">RAS Custom-Scripting</a>



<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>



<a href="https://msdn.microsoft.com/aba43ef9-7f62-48ab-a790-c8592a57f2c2">RasFreeBuffer</a>
 

 

