---
UID: NF:tapi3cc.IEnumAgentHandler.Reset
title: IEnumAgentHandler::Reset
author: windows-sdk-content
description: The Reset method resets the enumeration sequence to the beginning.
old-location: tapi3\ienumagenthandler_reset.htm
old-project: Tapi
ms.assetid: cb113db5-718d-4c5e-92ad-4eb605911c71
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IEnumAgentHandler interface [TAPI 2.2],Reset method, IEnumAgentHandler.Reset, IEnumAgentHandler::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumAgentHandler interface, _tapi3_ienumagenthandler_reset, tapi3.ienumagenthandler_reset, tapi3cc/IEnumAgentHandler::Reset
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
req.typenames: AGENT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	IEnumAgentHandler.Reset
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumAgentHandler::Reset


## -description


The 
<b>Reset</b> method resets the enumeration sequence to the beginning.


## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a318318a-769e-4619-a461-4988d90d3f1a">IEnumAgentHandler</a>
 

 

