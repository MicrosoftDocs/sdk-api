---
UID: NC:ras.PFNRASRETRIEVEBUFFER
title: PFNRASRETRIEVEBUFFER
author: windows-sdk-content
description: The custom-scripting DLL calls the RasRetrieveBuffer function to obtain data received from the RAS server over the specified port.
old-location: rras\rasretrievebuffer.htm
tech.root: rras
ms.assetid: 5dc8a034-f1cb-47c5-8d60-06f314a85f11
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: PFNRASRETRIEVEBUFFER, PFNRASRETRIEVEBUFFER callback, RasRetrieveBuffer, RasRetrieveBuffer callback function [RAS], _ras_rasretrievebuffer, ras/RasRetrieveBuffer, rras.rasretrievebuffer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasRetrieveBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNRASRETRIEVEBUFFER callback function


## -description


The custom-scripting DLL calls the 
<i>RasRetrieveBuffer</i> function to obtain data received from the RAS server over the specified port. The custom-scripting DLL should call 
<i>RasRetrieveBuffer</i> only after RAS has signaled the event object passed in the call to 
<a href="https://msdn.microsoft.com/cc5523df-748d-4f96-8d54-bf0a2f9ecde4">RasReceiveBuffer</a>.

The <a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">PFNRASRETRIEVEBUFFER</a> type defines a pointer to this callback function. <i>RasRetrieveBuffer</i> is a placeholder for the application-defined function name.


## -parameters




### -param hPort

Handle to the port on which to receive the data. This handle should be the handle passed in by RAS as the first parameter of the 
<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a> function.


### -param pBuffer

Pointer to a buffer to receive the data from the port specified by the <i>hPort</i> parameter. Obtain this buffer using 
<a href="https://msdn.microsoft.com/655f2dfa-a6cf-43db-8d2e-bf9a10163c75">RasGetBuffer</a> function. The value of this parameter may be the same as the pointer to the buffer passed into the 
<a href="https://msdn.microsoft.com/cc5523df-748d-4f96-8d54-bf0a2f9ecde4">RasReceiveBuffer</a> function.


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
<a href="https://msdn.microsoft.com/cc5523df-748d-4f96-8d54-bf0a2f9ecde4">RasReceiveBuffer</a>.

The custom-scripting DLL calls 
<i>RasRetrieveBuffer</i> through a function pointer. The function pointer is passed to the custom-scripting DLL as a parameter when RAS calls the DLL's implementation of 
<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>.




## -see-also




<a href="https://msdn.microsoft.com/c27b8b02-6018-4441-a355-1fb890b9001c">RAS Custom-Scripting</a>



<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>



<a href="https://msdn.microsoft.com/cc5523df-748d-4f96-8d54-bf0a2f9ecde4">RasReceiveBuffer</a>



<a href="https://msdn.microsoft.com/157a2bc7-351f-4170-b85b-ed789b4997ab">RasSendBuffer</a>
 

 

