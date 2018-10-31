---
UID: NF:tapi3.ITAgentHandler.EnumerateACDGroups
title: ITAgentHandler::EnumerateACDGroups
author: windows-sdk-content
description: The EnumerateACDGroups method enumerates ACD groups currently associated with the agent handler.
old-location: tapi3\itagenthandler_enumerateacdgroups.htm
tech.root: tapi
ms.assetid: a9078166-ff6a-4520-8209-e785bd6e7100
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EnumerateACDGroups, EnumerateACDGroups method [TAPI 2.2], EnumerateACDGroups method [TAPI 2.2],ITAgentHandler interface, ITAgentHandler interface [TAPI 2.2],EnumerateACDGroups method, ITAgentHandler.EnumerateACDGroups, ITAgentHandler::EnumerateACDGroups, _tapi3_itagenthandler_enumerateacdgroups, tapi3.itagenthandler_enumerateacdgroups, tapi3cc/ITAgentHandler::EnumerateACDGroups
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentHandler.EnumerateACDGroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgentHandler::EnumerateACDGroups


## -description


The 
<b>EnumerateACDGroups</b> method enumerates ACD groups currently associated with the agent handler. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/72dcc4c8-fac6-4635-995e-18a5693da99b">get_ACDGroups</a> method. The number of groups returned is based upon replies from the ACD proxy application. Each proxy application will return a list of groups according to its own internal privilege/security decisions.


## -parameters




### -param ppEnumACDGroup [out]

Pointer to 
<a href="https://msdn.microsoft.com/301cd27e-00ac-44a4-b5c6-0efcb36ad974">IEnumACDGroup</a> interface.


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
The <i>ppEnumACDGroup</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/301cd27e-00ac-44a4-b5c6-0efcb36ad974">IEnumACDGroup</a> interface returned by <b>ITAgentHandler::EnumerateACDGroups</b>. The application must call <b>Release</b> on the 
<b>IEnumACDGroup</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/301cd27e-00ac-44a4-b5c6-0efcb36ad974">IEnumACDGroup</a>



<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a>
 

 

