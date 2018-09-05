---
UID: NC:ras.PFNRASRECEIVEBUFFER
title: PFNRASRECEIVEBUFFER
author: windows-sdk-content
description: The custom-scripting DLL calls the RasReceiveBuffer function to inform RAS that it is ready to receive data from the server over the specified port.
old-location: rras\rasreceivebuffer.htm
old-project: RRAS
ms.assetid: cc5523df-748d-4f96-8d54-bf0a2f9ecde4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PFNRASRECEIVEBUFFER, PFNRASRECEIVEBUFFER callback, RasReceiveBuffer, RasReceiveBuffer callback function [RAS], _ras_rasreceivebuffer, ras/RasReceiveBuffer, rras.rasreceivebuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ras.h
req.include-header: 
req.redist: 
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
 - RasReceiveBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PFNRASRECEIVEBUFFER callback function


## -description


The custom-scripting DLL calls the 
<i>RasReceiveBuffer</i> function to inform RAS that it is ready to receive data from the server over the specified port.

The <a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">PFNRASRECEIVEBUFFER</a> type defines a pointer to this callback function. <i>RasReceiveBuffer</i> is a placeholder for the application-defined function name.


## -parameters




### -param hPort

Handle to the port on which to receive the data. This handle should be the handle passed in by RAS as the first parameter of the 
<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a> function.


### -param pBuffer

Pointer to a buffer to receive the data from the port specified by the <i>hPort</i> parameter. Obtain this buffer using 
<a href="https://msdn.microsoft.com/655f2dfa-a6cf-43db-8d2e-bf9a10163c75">RasGetBuffer</a> function.


### -param pdwSize

Pointer to a <b>DWORD</b> variable that receives the size of the data returned in the buffer pointed to by the <i>pBuffer</i> parameter.


### -param dwTimeOut


### -param hEvent

Handle to an event object that RAS will signal when the received data is available.


#### - dwTimeout

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
<a href="https://msdn.microsoft.com/5dc8a034-f1cb-47c5-8d60-06f314a85f11">RasRetrieveBuffer</a> function to obtain the data. The custom-scripting DLL may pass the same buffer pointer in 
<b>RasRetrieveBuffer</b> that it passed in <b>RasReceiveBuffer</b>.

RAS also signals the event object if, for some reason, the port is disconnected before the data is posted. In this case, 
<a href="https://msdn.microsoft.com/5dc8a034-f1cb-47c5-8d60-06f314a85f11">RasRetrieveBuffer</a> returns an error defined in Raserror.h, that indicates the cause of the failure.

The custom-scripting DLL calls 
<i>RasReceiveBuffer</i> through a function pointer. The function pointer is passed to the custom-scripting DLL as a parameter when RAS calls the DLL's implementation of 
<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>.




## -see-also




<a href="https://msdn.microsoft.com/c27b8b02-6018-4441-a355-1fb890b9001c">RAS Custom-Scripting</a>



<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>



<a href="https://msdn.microsoft.com/157a2bc7-351f-4170-b85b-ed789b4997ab">RasSendBuffer</a>
 

 

