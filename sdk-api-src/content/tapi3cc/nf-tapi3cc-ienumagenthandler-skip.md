---
UID: NF:tapi3cc.IEnumAgentHandler.Skip
title: IEnumAgentHandler::Skip
author: windows-driver-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumagenthandler_skip.htm
old-project: Tapi
ms.assetid: cf6b7003-13f1-4203-b341-2c9796cffdd2
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IEnumAgentHandler interface [TAPI 2.2],Skip method, IEnumAgentHandler.Skip, IEnumAgentHandler::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumAgentHandler interface, _tapi3_ienumagenthandler_skip, tapi3.ienumagenthandler_skip, tapi3cc/IEnumAgentHandler::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IEnumAgentHandler.Skip
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumAgentHandler::Skip


## -description


The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


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
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

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
 

 

