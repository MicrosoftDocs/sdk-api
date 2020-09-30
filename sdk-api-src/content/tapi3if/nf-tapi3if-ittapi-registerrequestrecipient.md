---
UID: NF:tapi3if.ITTAPI.RegisterRequestRecipient
title: ITTAPI::RegisterRequestRecipient (tapi3if.h)
description: The RegisterRequestRecipient method registers an application instance as being the proper one to handle assisted telephony requests.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","RegisterRequestRecipient method","ITTAPI.RegisterRequestRecipient","ITTAPI::RegisterRequestRecipient","RegisterRequestRecipient","RegisterRequestRecipient method [TAPI 2.2]","RegisterRequestRecipient method [TAPI 2.2]","ITTAPI interface","_tapi3_ittapi_registerrequestrecipient","tapi3.ittapi_registerrequestrecipient","tapi3if/ITTAPI::RegisterRequestRecipient"]
old-location: tapi3\ittapi_registerrequestrecipient.htm
tech.root: tapi3
ms.assetid: bee5348e-99f0-4168-9021-112fc16d8921
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],RegisterRequestRecipient method, ITTAPI.RegisterRequestRecipient, ITTAPI::RegisterRequestRecipient, RegisterRequestRecipient, RegisterRequestRecipient method [TAPI 2.2], RegisterRequestRecipient method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_registerrequestrecipient, tapi3.ittapi_registerrequestrecipient, tapi3if/ITTAPI::RegisterRequestRecipient
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
 - ITTAPI::RegisterRequestRecipient
 - tapi3if/ITTAPI::RegisterRequestRecipient
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
 - ITTAPI.RegisterRequestRecipient
---

# ITTAPI::RegisterRequestRecipient


## -description

The 
<b>RegisterRequestRecipient</b> method registers an application instance as being the proper one to handle assisted telephony requests.

## -parameters

### -param lRegistrationInstance [in]

Pointer to registration instance.

### -param lRequestMode [in]

Request mode.

### -param fEnable [in]

VARIANT_TRUE indicates that the caller wants to register as the handler; VARIANT_FALSE that it wants to unregister as the handler.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The TAPI object has not been initialized.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itrequest">ITRequest</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itrequestevent">ITRequestEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall">MakeCall</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>