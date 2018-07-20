---
UID: NF:tapi3cc.ITAgentHandler.get_ACDGroups
title: ITAgentHandler::get_ACDGroups
author: windows-sdk-content
description: The get_ACDGroups method creates a collection of ACD groups currently associated with the agent handler.
old-location: tapi3\itagenthandler_get_acdgroups.htm
old-project: tapi
ms.assetid: 72dcc4c8-fac6-4635-995e-18a5693da99b
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITAgentHandler interface [TAPI 2.2],get_ACDGroups method, ITAgentHandler.get_ACDGroups, ITAgentHandler::get_ACDGroups, _tapi3_itagenthandler_get_acdgroups, get_ACDGroups, get_ACDGroups method [TAPI 2.2], get_ACDGroups method [TAPI 2.2],ITAgentHandler interface, tapi3.itagenthandler_get_acdgroups, tapi3cc/ITAgentHandler::get_ACDGroups
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
 - ITAgentHandler.get_ACDGroups
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentHandler::get_ACDGroups


## -description


The 
<b>get_ACDGroups</b> method creates a collection of ACD groups currently associated with the agent handler. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/a9078166-ff6a-4520-8209-e785bd6e7100">EnumerateACDGroups</a> method.


## -parameters




### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface pointers (ACD group objects).


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
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface returned by <b>ITAgentHandler::get_ACDGroups</b>. The application must call <b>Release</b> on the 
<b>ITACDGroup</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/a9078166-ff6a-4520-8209-e785bd6e7100">EnumerateACDGroups</a>



<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a>



<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>
 

 

