---
UID: NF:tapi3cc.IEnumAgentHandler.Clone
title: IEnumAgentHandler::Clone
author: windows-sdk-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.
old-location: tapi3\ienumagenthandler_clone.htm
old-project: tapi
ms.assetid: a7358d0d-6d5a-4845-a212-d278a8d2b7fe
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumAgentHandler interface, IEnumAgentHandler interface [TAPI 2.2],Clone method, IEnumAgentHandler.Clone, IEnumAgentHandler::Clone, _tapi3_ienumagenthandler_clone, tapi3.ienumagenthandler_clone, tapi3cc/IEnumAgentHandler::Clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3cc.h
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
req.typenames: AGENT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumAgentHandler.Clone
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumAgentHandler::Clone


## -description


The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppEnum [out]

Pointer to new 
<a href="https://msdn.microsoft.com/a318318a-769e-4619-a461-4988d90d3f1a">IEnumAgentHandler</a> interface.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter is not a valid pointer.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/a318318a-769e-4619-a461-4988d90d3f1a">IEnumAgentHandler</a> interface returned by <b>IEnumAgentHandler::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumAgentHandler</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/a318318a-769e-4619-a461-4988d90d3f1a">IEnumAgentHandler</a>
 

 

