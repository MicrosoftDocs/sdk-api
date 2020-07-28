---
UID: NF:tapi3.IEnumAgentHandler.Skip
title: IEnumAgentHandler::Skip (tapi3.h)
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumAgentHandler interface [TAPI 2.2]","Skip method","IEnumAgentHandler.Skip","IEnumAgentHandler::Skip","Skip","Skip method [TAPI 2.2]","Skip method [TAPI 2.2]","IEnumAgentHandler interface","_tapi3_ienumagenthandler_skip","tapi3.ienumagenthandler_skip","tapi3cc/IEnumAgentHandler::Skip"]
old-location: tapi3\ienumagenthandler_skip.htm
tech.root: tapi3
ms.assetid: cf6b7003-13f1-4203-b341-2c9796cffdd2
ms.date: 12/05/2018
ms.keywords: IEnumAgentHandler interface [TAPI 2.2],Skip method, IEnumAgentHandler.Skip, IEnumAgentHandler::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumAgentHandler interface, _tapi3_ienumagenthandler_skip, tapi3.ienumagenthandler_skip, tapi3cc/IEnumAgentHandler::Skip
f1_keywords:
- tapi3/IEnumAgentHandler.Skip
dev_langs:
- c++
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
- IEnumAgentHandler.Skip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a>
 

 

