---
UID: NC:ras.PFNRASRECEIVEBUFFER
title: PFNRASRECEIVEBUFFER (ras.h)
description: The custom-scripting DLL calls the RasReceiveBuffer function to inform RAS that it is ready to receive data from the server over the specified port.
helpviewer_keywords: ["PFNRASRECEIVEBUFFER","PFNRASRECEIVEBUFFER callback","RasReceiveBuffer","RasReceiveBuffer callback function [RAS]","_ras_rasreceivebuffer","ras/RasReceiveBuffer","rras.rasreceivebuffer"]
old-location: rras\rasreceivebuffer.htm
tech.root: RRAS
ms.assetid: cc5523df-748d-4f96-8d54-bf0a2f9ecde4
ms.date: 12/05/2018
ms.keywords: PFNRASRECEIVEBUFFER, PFNRASRECEIVEBUFFER callback, RasReceiveBuffer, RasReceiveBuffer callback function [RAS], _ras_rasreceivebuffer, ras/RasReceiveBuffer, rras.rasreceivebuffer
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
 - PFNRASRECEIVEBUFFER
 - ras/PFNRASRECEIVEBUFFER
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
 - RasReceiveBuffer
---

# PFNRASRECEIVEBUFFER callback function


## -description

The custom-scripting DLL calls the 
<i>RasReceiveBuffer</i> function to inform RAS that it is ready to receive data from the server over the specified port.

The <a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">PFNRASRECEIVEBUFFER</a> type defines a pointer to this callback function. <i>RasReceiveBuffer</i> is a placeholder for the application-defined function name.

## -parameters

### -param hPort

Handle to the port on which to receive the data. This handle should be the handle passed in by RAS as the first parameter of the 
<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a> function.

### -param pBuffer

Pointer to a buffer to receive the data from the port specified by the <i>hPort</i> parameter. Obtain this buffer using 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasgetbuffer">RasGetBuffer</a> function.

### -param pdwSize

Pointer to a <b>DWORD</b> variable that receives the size of the data returned in the buffer pointed to by the <i>pBuffer</i> parameter.

### -param dwTimeOut

### -param hEvent

Handle to an event object that RAS will signal when the received data is available.

### -param dwTimeout

Specifies a time-out period in milliseconds after which the custom-scripting DLL will no longer wait for the data.

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

<i>RasReceiveBuffer</i> is an asynchronous function. 
<i>RasReceiveBuffer</i> returns immediately even if the data is not yet available. The custom-scripting DLL must wait on the event object specified by the <i>hEvent</i> parameter. When the data is available, RAS signals this event. The custom-scripting DLL should then call the 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasretrievebuffer">RasRetrieveBuffer</a> function to obtain the data. The custom-scripting DLL may pass the same buffer pointer in 
<b>RasRetrieveBuffer</b> that it passed in <b>RasReceiveBuffer</b>.

RAS also signals the event object if, for some reason, the port is disconnected before the data is posted. In this case, 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasretrievebuffer">RasRetrieveBuffer</a> returns an error defined in Raserror.h, that indicates the cause of the failure.

The custom-scripting DLL calls 
<i>RasReceiveBuffer</i> through a function pointer. The function pointer is passed to the custom-scripting DLL as a parameter when RAS calls the DLL's implementation of 
<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>.

## -see-also

<a href="/windows/desktop/RRAS/ras-custom-scripting">RAS Custom-Scripting</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrassendbuffer">RasSendBuffer</a>