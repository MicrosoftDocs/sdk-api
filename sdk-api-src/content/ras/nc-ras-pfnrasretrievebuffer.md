---
UID: NC:ras.PFNRASRETRIEVEBUFFER
title: PFNRASRETRIEVEBUFFER (ras.h)
description: The custom-scripting DLL calls the RasRetrieveBuffer function to obtain data received from the RAS server over the specified port.
helpviewer_keywords: ["PFNRASRETRIEVEBUFFER","PFNRASRETRIEVEBUFFER callback","RasRetrieveBuffer","RasRetrieveBuffer callback function [RAS]","_ras_rasretrievebuffer","ras/RasRetrieveBuffer","rras.rasretrievebuffer"]
old-location: rras\rasretrievebuffer.htm
tech.root: RRAS
ms.assetid: 5dc8a034-f1cb-47c5-8d60-06f314a85f11
ms.date: 12/05/2018
ms.keywords: PFNRASRETRIEVEBUFFER, PFNRASRETRIEVEBUFFER callback, RasRetrieveBuffer, RasRetrieveBuffer callback function [RAS], _ras_rasretrievebuffer, ras/RasRetrieveBuffer, rras.rasretrievebuffer
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
 - PFNRASRETRIEVEBUFFER
 - ras/PFNRASRETRIEVEBUFFER
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
 - RasRetrieveBuffer
---

# PFNRASRETRIEVEBUFFER callback function


## -description

The custom-scripting DLL calls the 
<i>RasRetrieveBuffer</i> function to obtain data received from the RAS server over the specified port. The custom-scripting DLL should call 
<i>RasRetrieveBuffer</i> only after RAS has signaled the event object passed in the call to 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasreceivebuffer">RasReceiveBuffer</a>.

The <a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">PFNRASRETRIEVEBUFFER</a> type defines a pointer to this callback function. <i>RasRetrieveBuffer</i> is a placeholder for the application-defined function name.

## -parameters

### -param hPort

Handle to the port on which to receive the data. This handle should be the handle passed in by RAS as the first parameter of the 
<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a> function.

### -param pBuffer

Pointer to a buffer to receive the data from the port specified by the <i>hPort</i> parameter. Obtain this buffer using 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasgetbuffer">RasGetBuffer</a> function. The value of this parameter may be the same as the pointer to the buffer passed into the 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasreceivebuffer">RasReceiveBuffer</a> function.

### -param pdwSize

Pointer to a <b>DWORD</b> variable that receives the size of the data returned in the buffer pointed to by the <i>pBuffer</i> parameter.

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
 

RAS signals the event object if the port gets disconnected for some reason before the data is posted. In this case, 
<i>RasRetrieveBuffer</i> returns an error defined in Raserror.h, that indicates the cause of the failure.

## -remarks

The 
<i>RasRetrieveBuffer</i> function is synchronous. When it returns, the buffer pointed to by the <i>pBuffer</i> parameter contains the data received over the specified port. The custom-scripting DLL should call 
<i>RasRetrieveBuffer</i> only after RAS has signaled the event object that the DLL passed in the call to 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasreceivebuffer">RasReceiveBuffer</a>.

The custom-scripting DLL calls 
<i>RasRetrieveBuffer</i> through a function pointer. The function pointer is passed to the custom-scripting DLL as a parameter when RAS calls the DLL's implementation of 
<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>.

## -see-also

<a href="/windows/desktop/RRAS/ras-custom-scripting">RAS Custom-Scripting</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrasreceivebuffer">RasReceiveBuffer</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrassendbuffer">RasSendBuffer</a>