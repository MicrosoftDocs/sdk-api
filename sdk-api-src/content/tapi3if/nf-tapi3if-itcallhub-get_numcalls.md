---
UID: NF:tapi3if.ITCallHub.get_NumCalls
title: ITCallHub::get_NumCalls (tapi3if.h)
description: The get_NumCalls method gets the number of calls currently in the CallHub.
helpviewer_keywords: ["ITCallHub interface [TAPI 2.2]","get_NumCalls method","ITCallHub.get_NumCalls","ITCallHub::get_NumCalls","_tapi3_itcallhub_get_numcalls","get_NumCalls","get_NumCalls method [TAPI 2.2]","get_NumCalls method [TAPI 2.2]","ITCallHub interface","tapi3.itcallhub_get_numcalls","tapi3if/ITCallHub::get_NumCalls"]
old-location: tapi3\itcallhub_get_numcalls.htm
tech.root: tapi3
ms.assetid: 52313969-ce8e-43da-8844-b4d0834dd446
ms.date: 12/05/2018
ms.keywords: ITCallHub interface [TAPI 2.2],get_NumCalls method, ITCallHub.get_NumCalls, ITCallHub::get_NumCalls, _tapi3_itcallhub_get_numcalls, get_NumCalls, get_NumCalls method [TAPI 2.2], get_NumCalls method [TAPI 2.2],ITCallHub interface, tapi3.itcallhub_get_numcalls, tapi3if/ITCallHub::get_NumCalls
f1_keywords:
- tapi3if/ITCallHub.get_NumCalls
dev_langs:
- c++
req.header: tapi3if.h
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
- ITCallHub.get_NumCalls
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallHub::get_NumCalls


## -description


The 
<b>get_NumCalls</b> method gets the number of calls currently in the CallHub.


## -parameters




### -param plCalls [out]

Total number of calls in the CallHub.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plCalls</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/callhub-object">CallHub Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a>
 

 

