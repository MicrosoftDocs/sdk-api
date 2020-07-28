---
UID: NF:tapi3cc.IEnumAgentHandler.Next
title: IEnumAgentHandler::Next (tapi3cc.h)
description: The Next method gets the next specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumAgentHandler interface [TAPI 2.2]","Next method","IEnumAgentHandler.Next","IEnumAgentHandler::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumAgentHandler interface","_tapi3_ienumagenthandler_next","tapi3.ienumagenthandler_next","tapi3cc/IEnumAgentHandler::Next"]
old-location: tapi3\ienumagenthandler_next.htm
tech.root: tapi3
ms.assetid: 0e6a7db0-c339-4a36-aea8-e3f9f2d5cd09
ms.date: 12/05/2018
ms.keywords: IEnumAgentHandler interface [TAPI 2.2],Next method, IEnumAgentHandler.Next, IEnumAgentHandler::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumAgentHandler interface, _tapi3_ienumagenthandler_next, tapi3.ienumagenthandler_next, tapi3cc/IEnumAgentHandler::Next
f1_keywords:
- tapi3cc/IEnumAgentHandler.Next
dev_langs:
- c++
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
- IEnumAgentHandler.Next
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumAgentHandler::Next


## -description


The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements requested.


### -param ppElements [out]

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interfaces.


### -param pceltFetched [out]

Pointer to number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.


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
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppElements</i> parameter is not a valid pointer.

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
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a> interface returned by <b>IEnumAgentHandler::Next</b>. The application must call <b>Release</b> on the 
<b>IEnumAgentHandler</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a>
 

 

