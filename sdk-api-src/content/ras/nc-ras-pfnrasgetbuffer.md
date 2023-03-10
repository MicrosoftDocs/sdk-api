---
UID: NC:ras.PFNRASGETBUFFER
title: PFNRASGETBUFFER (ras.h)
description: The custom-scripting DLL calls RasGetBuffer to allocate memory for sending or receiving data over the port connected to the server.
helpviewer_keywords: ["PFNRASGETBUFFER","PFNRASGETBUFFER callback","RasGetBuffer","RasGetBuffer callback function [RAS]","_ras_rasgetbuffer","ras/RasGetBuffer","rras.rasgetbuffer"]
old-location: rras\rasgetbuffer.htm
tech.root: RRAS
ms.assetid: 655f2dfa-a6cf-43db-8d2e-bf9a10163c75
ms.date: 12/05/2018
ms.keywords: PFNRASGETBUFFER, PFNRASGETBUFFER callback, RasGetBuffer, RasGetBuffer callback function [RAS], _ras_rasgetbuffer, ras/RasGetBuffer, rras.rasgetbuffer
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNRASGETBUFFER
 - ras/PFNRASGETBUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasGetBuffer
---

# PFNRASGETBUFFER callback function


## -description

The custom-scripting DLL calls 
<i>RasGetBuffer</i> to allocate memory for sending or receiving data over the port connected to the server.

## -parameters

### -param ppBuffer

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
<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>.

## -see-also

<a href="/windows/desktop/RRAS/ras-custom-scripting">RAS Custom-Scripting</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrasfreebuffer">RasFreeBuffer</a>
