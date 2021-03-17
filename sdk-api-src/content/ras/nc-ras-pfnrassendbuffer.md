---
UID: NC:ras.PFNRASSENDBUFFER
title: PFNRASSENDBUFFER (ras.h)
description: The custom-scripting DLL calls the RasSendBuffer function to send data to the server over the specified port.
helpviewer_keywords: ["PFNRASSENDBUFFER","PFNRASSENDBUFFER callback","RasSendBuffer","RasSendBuffer callback function [RAS]","_ras_rassendbuffer","ras/RasSendBuffer","rras.rassendbuffer"]
old-location: rras\rassendbuffer.htm
tech.root: RRAS
ms.assetid: 157a2bc7-351f-4170-b85b-ed789b4997ab
ms.date: 12/05/2018
ms.keywords: PFNRASSENDBUFFER, PFNRASSENDBUFFER callback, RasSendBuffer, RasSendBuffer callback function [RAS], _ras_rassendbuffer, ras/RasSendBuffer, rras.rassendbuffer
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
 - PFNRASSENDBUFFER
 - ras/PFNRASSENDBUFFER
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
 - RasSendBuffer
---

# PFNRASSENDBUFFER callback function


## -description

The custom-scripting DLL calls the 
<i>RasSendBuffer</i> function to send data to the server over the specified port.

The <a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">PFNRASSENDBUFFER</a> type of the <b>RasCustomScriptExecute</b> callback defines a pointer to this function. <i>RasSendBuffer</i> is a placeholder for the application-defined function name.

## -parameters

### -param hPort

Handle to the port on which to send the data in the buffer. This handle should be the handle passed in by RAS as the first parameter of the 
<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a> function.

### -param pBuffer

Pointer to a buffer of data to send over the port specified by the <i>hPort</i> parameter. Obtain this buffer using 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasgetbuffer">RasGetBuffer</a> function.

### -param dwSize

Specifies the size of the data in the buffer pointed to by the <i>pBuffer</i> parameter.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value can be one of the following error codes.

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
<i>RasSendBuffer</i> through a function pointer. The function pointer is passed to the custom-scripting DLL as a parameter when RAS calls the DLL's implementation of 
<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>.

## -see-also

<a href="/windows/desktop/RRAS/ras-custom-scripting">RAS Custom-Scripting</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrasreceivebuffer">RasReceiveBuffer</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrasretrievebuffer">RasRetrieveBuffer</a>