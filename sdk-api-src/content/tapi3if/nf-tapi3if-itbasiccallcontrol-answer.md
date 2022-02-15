---
UID: NF:tapi3if.ITBasicCallControl.Answer
title: ITBasicCallControl::Answer (tapi3if.h)
description: The Answer method answers an incoming call. This method can succeed only if the call state is CS_OFFERING.
helpviewer_keywords: ["Answer","Answer method [TAPI 2.2]","Answer method [TAPI 2.2]","ITBasicCallControl interface","ITBasicCallControl interface [TAPI 2.2]","Answer method","ITBasicCallControl.Answer","ITBasicCallControl::Answer","_tapi3_itbasiccallcontrol_answer","tapi3.itbasiccallcontrol_answer","tapi3if/ITBasicCallControl::Answer"]
old-location: tapi3\itbasiccallcontrol_answer.htm
tech.root: tapi3
ms.assetid: 81928cf7-082e-44e1-a631-a50a1f01ecec
ms.date: 12/05/2018
ms.keywords: Answer, Answer method [TAPI 2.2], Answer method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Answer method, ITBasicCallControl.Answer, ITBasicCallControl::Answer, _tapi3_itbasiccallcontrol_answer, tapi3.itbasiccallcontrol_answer, tapi3if/ITBasicCallControl::Answer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITBasicCallControl::Answer
 - tapi3if/ITBasicCallControl::Answer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl.Answer
---

# ITBasicCallControl::Answer


## -description

The 
<b>Answer</b> method answers an incoming call. This method can succeed only if the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">call state</a> is CS_OFFERING.



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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Call state was not CS_OFFERING.

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

## -see-also

<a href="/windows/desktop/Tapi/answer-ovr">Answer Overview</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineanswer">lineAnswer</a>
