---
UID: NF:tapi3if.ITTAPI.EnumerateCallHubs
title: ITTAPI::EnumerateCallHubs (tapi3if.h)
description: The EnumerateCallHubs method enumerates the currently available call hubs. Provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_Callhubs method.
helpviewer_keywords: ["EnumerateCallHubs","EnumerateCallHubs method [TAPI 2.2]","EnumerateCallHubs method [TAPI 2.2]","ITTAPI interface","ITTAPI interface [TAPI 2.2]","EnumerateCallHubs method","ITTAPI.EnumerateCallHubs","ITTAPI::EnumerateCallHubs","_tapi3_ittapi_enumeratecallhubs","tapi3.ittapi_enumeratecallhubs","tapi3if/ITTAPI::EnumerateCallHubs"]
old-location: tapi3\ittapi_enumeratecallhubs.htm
tech.root: tapi3
ms.assetid: 98d20aa3-6d4c-4971-aa4a-5b9632038eb1
ms.date: 12/05/2018
ms.keywords: EnumerateCallHubs, EnumerateCallHubs method [TAPI 2.2], EnumerateCallHubs method [TAPI 2.2],ITTAPI interface, ITTAPI interface [TAPI 2.2],EnumerateCallHubs method, ITTAPI.EnumerateCallHubs, ITTAPI::EnumerateCallHubs, _tapi3_ittapi_enumeratecallhubs, tapi3.ittapi_enumeratecallhubs, tapi3if/ITTAPI::EnumerateCallHubs
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
 - ITTAPI::EnumerateCallHubs
 - tapi3if/ITTAPI::EnumerateCallHubs
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
 - ITTAPI.EnumerateCallHubs
---

# ITTAPI::EnumerateCallHubs


## -description

The 
<b>EnumerateCallHubs</b> method enumerates the currently available call hubs. Provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_callhubs">get_Callhubs</a> method.

## -parameters

### -param ppEnumCallHub [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub">IEnumCallHub</a> interface.

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
The <i>ppEnumCallHub</i> parameter is not a valid pointer.

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

## -remarks

TAPI calls the <b>Addref</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub">IEnumCallHub</a> interface returned by <b>ITTAPI::EnumerateCallHubs</b>. The application must call <b>Release</b> on the 
<b>IEnumCallHub</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub">IEnumCallHub</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>