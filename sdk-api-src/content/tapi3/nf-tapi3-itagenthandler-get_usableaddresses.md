---
UID: NF:tapi3.ITAgentHandler.get_UsableAddresses
title: ITAgentHandler::get_UsableAddresses
author: windows-sdk-content
description: The get_UsableAddresses method creates a collection of addresses available for receiving ACD calls on this agent handler.
old-location: tapi3\itagenthandler_get_usableaddresses.htm
old-project: tapi
ms.assetid: ee457b5c-e505-489c-93dc-8bdfb87c7afe
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAgentHandler interface [TAPI 2.2],get_UsableAddresses method, ITAgentHandler.get_UsableAddresses, ITAgentHandler::get_UsableAddresses, _tapi3_itagenthandler_get_usableaddresses, get_UsableAddresses, get_UsableAddresses method [TAPI 2.2], get_UsableAddresses method [TAPI 2.2],ITAgentHandler interface, tapi3.itagenthandler_get_usableaddresses, tapi3cc/ITAgentHandler::get_UsableAddresses
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3.h
req.include-header: Tapi3.h
req.redist: 
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
 - ITAgentHandler.get_UsableAddresses
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentHandler::get_UsableAddresses


## -description


The 
<b>get_UsableAddresses</b> method creates a collection of addresses available for receiving ACD calls on this agent handler. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/9821b073-c64b-4f2b-b771-6bf027f9aa70">EnumerateUsableAddresses</a> method.


## -parameters




### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface pointers (address objects).


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
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface returned by <b>ITAgentHandler::get_UsableAddresses</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/9821b073-c64b-4f2b-b771-6bf027f9aa70">EnumerateUsableAddresses</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>
 

 

