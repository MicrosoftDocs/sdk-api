---
UID: NF:tapi3.ITAgentHandler.CreateAgent
title: ITAgentHandler::CreateAgent
author: windows-sdk-content
description: The CreateAgent method creates an Agent object.
old-location: tapi3\itagenthandler_createagent.htm
old-project: tapi
ms.assetid: f3242013-59a6-40f9-9bb1-0bc30f27311c
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: CreateAgent, CreateAgent method [TAPI 2.2], CreateAgent method [TAPI 2.2],ITAgentHandler interface, ITAgentHandler interface [TAPI 2.2],CreateAgent method, ITAgentHandler.CreateAgent, ITAgentHandler::CreateAgent, _tapi3_itagenthandler_createagent, tapi3.itagenthandler_createagent, tapi3cc/ITAgentHandler::CreateAgent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3.h
req.include-header: Tapi3.h
req.target-type: Windows
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
tech.root: 
req.typenames: MSP_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentHandler.CreateAgent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentHandler::CreateAgent


## -description


The 
<b>CreateAgent</b> method creates an Agent object.


## -parameters




### -param ppAgent [out]

Pointer to the 
<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppAgent</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a> interface returned by <b>ITAgentHandler::CreateAgent</b>. The application must call <b>Release</b> on the 
<b>ITAgent</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/95c70e48-b990-47c7-a8b8-5fa3a84ec5ba">CreateAgentWithID</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a>
 

 

