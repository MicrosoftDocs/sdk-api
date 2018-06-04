---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PxeRegisterCallback function


## -description


Registers callback functions for different notification events.


## -parameters




### -param hProvider [in]

<b>HANDLE</b> passed to the 
      <a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a> function.


### -param CallbackType [in]

Specifies the callback that is being registered.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_CALLBACK_RECV_REQUEST"></a><a id="pxe_callback_recv_request"></a><dl>
<dt><b>PXE_CALLBACK_RECV_REQUEST</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Register the <a href="https://msdn.microsoft.com/704972d5-177a-490e-881f-d2b3025babda">PxeProviderRecvRequest</a> 
        callback. This callback must be registered while the provider is processing the 
        <a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a> function or the 
        provider will be shut down.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_CALLBACK_SHUTDOWN"></a><a id="pxe_callback_shutdown"></a><dl>
<dt><b>PXE_CALLBACK_SHUTDOWN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Register the <a href="https://msdn.microsoft.com/436d7428-18f9-4b73-b346-79c9a0738c31">PxeProviderShutdown</a> 
        callback. This callback must be registered while the provider is processing the 
        <a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a> function or the 
        provider will be shut down.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_CALLBACK_SERVICE_CONTROL"></a><a id="pxe_callback_service_control"></a><dl>
<dt><b>PXE_CALLBACK_SERVICE_CONTROL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Register the 
        <a href="https://msdn.microsoft.com/180ddcda-d111-4c81-9177-db99cbf1449f">PxeProviderServiceControl</a> callback.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_CALLBACK_MAX"></a><a id="pxe_callback_max"></a><dl>
<dt><b>PXE_CALLBACK_MAX</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Used to determine an out-of-range index. Values greater than or equal to 
        <b>PXE_CALLBACK_MAX</b> are not valid.

</td>
</tr>
</table>
 


### -param pCallbackFunction [in]

Address of the callback function. The function signature varies depending on the 
      <i>CallbackType</i> parameter.


### -param pContext [in]

Context value to be passed to the callback function.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a>



<a href="https://msdn.microsoft.com/704972d5-177a-490e-881f-d2b3025babda">PxeProviderRecvRequest</a>



<a href="https://msdn.microsoft.com/180ddcda-d111-4c81-9177-db99cbf1449f">PxeProviderServiceControl</a>



<a href="https://msdn.microsoft.com/436d7428-18f9-4b73-b346-79c9a0738c31">PxeProviderShutdown</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

