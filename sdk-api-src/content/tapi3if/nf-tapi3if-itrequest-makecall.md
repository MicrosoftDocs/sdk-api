---
UID: NF:tapi3if.ITRequest.MakeCall
title: ITRequest::MakeCall (tapi3if.h)
description: The MakeCall method makes a call to the designated party.
helpviewer_keywords: ["ITRequest interface [TAPI 2.2]","MakeCall method","ITRequest.MakeCall","ITRequest::MakeCall","MakeCall","MakeCall method [TAPI 2.2]","MakeCall method [TAPI 2.2]","ITRequest interface","_tapi3_itrequest_makecall","tapi3.itrequest_makecall","tapi3if/ITRequest::MakeCall"]
old-location: tapi3\itrequest_makecall.htm
tech.root: tapi3
ms.assetid: 6896a18a-75ff-4f43-81e2-7b828bb16ff6
ms.date: 12/05/2018
ms.keywords: ITRequest interface [TAPI 2.2],MakeCall method, ITRequest.MakeCall, ITRequest::MakeCall, MakeCall, MakeCall method [TAPI 2.2], MakeCall method [TAPI 2.2],ITRequest interface, _tapi3_itrequest_makecall, tapi3.itrequest_makecall, tapi3if/ITRequest::MakeCall
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
 - ITRequest::MakeCall
 - tapi3if/ITRequest::MakeCall
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
 - ITRequest.MakeCall
---

# ITRequest::MakeCall


## -description

The 
<b>MakeCall</b> method makes a call to the designated party.

## -parameters

### -param pDestAddress [in]

Pointer to a <b>BSTR</b> containing the destination address for the call.

### -param pAppName [in]

Pointer to a <b>BSTR</b> containing the name of the application.

### -param pCalledParty [in]

Pointer to a <b>BSTR</b> containing the called party name.

### -param pComment [in]

Pointer to a <b>BSTR</b> containing a comment.

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
<dt><b>TAPIERR_NOREQUESTRECIPIENT</b></dt>
</dl>
</td>
<td width="60%">
No application exists that can handle the assisted telephony request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPIERR_INVALDESTADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The destination address is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPIERR_REQUESTQUEUEFULL</b></dt>
</dl>
</td>
<td width="60%">
The TAPI Server request queue is full and cannot handle another assisted telephony request.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDestAddress, pAppName, pCalledParty,</i> and <i>pComment</i> parameters. The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variables are no longer needed.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itrequest">ITRequest</a>