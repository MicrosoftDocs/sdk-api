---
UID: NF:tapi3cc.ITAgentHandler.EnumerateUsableAddresses
title: ITAgentHandler::EnumerateUsableAddresses
author: windows-sdk-content
description: The EnumerateUsableAddresses method enumerates addresses available for receiving ACD calls on this agent handler.
old-location: tapi3\itagenthandler_enumerateusableaddresses.htm
old-project: tapi
ms.assetid: 9821b073-c64b-4f2b-b771-6bf027f9aa70
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: EnumerateUsableAddresses, EnumerateUsableAddresses method [TAPI 2.2], EnumerateUsableAddresses method [TAPI 2.2],ITAgentHandler interface, ITAgentHandler interface [TAPI 2.2],EnumerateUsableAddresses method, ITAgentHandler.EnumerateUsableAddresses, ITAgentHandler::EnumerateUsableAddresses, _tapi3_itagenthandler_enumerateusableaddresses, tapi3.itagenthandler_enumerateusableaddresses, tapi3cc/ITAgentHandler::EnumerateUsableAddresses
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3cc.h
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
req.typenames: AGENT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentHandler.EnumerateUsableAddresses
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentHandler::EnumerateUsableAddresses


## -description


The 
<b>EnumerateUsableAddresses</b> method enumerates addresses available for receiving ACD calls on this agent handler. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/ee457b5c-e505-489c-93dc-8bdfb87c7afe">get_UsableAddresses</a> method.


## -parameters




### -param ppEnumAddress [out]

Pointer to 
<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a> interface.


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
The <i>ppEnumAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a> interface returned by <b>ITAgentHandler::EnumerateUsableAddresses</b>. The application must call <b>Release</b> on the 
<b>IEnumAddress</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a>
 

 

