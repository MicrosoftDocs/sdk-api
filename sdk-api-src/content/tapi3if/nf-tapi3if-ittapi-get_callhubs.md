---
UID: NF:tapi3if.ITTAPI.get_CallHubs
title: ITTAPI::get_CallHubs (tapi3if.h)
description: The get_CallHubs method creates a collection of the currently available call hubs. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateCallHubs method.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","get_CallHubs method","ITTAPI.get_CallHubs","ITTAPI::get_CallHubs","_tapi3_ittapi_get_callhubs","get_CallHubs","get_CallHubs method [TAPI 2.2]","get_CallHubs method [TAPI 2.2]","ITTAPI interface","tapi3.ittapi_get_callhubs","tapi3if/ITTAPI::get_CallHubs"]
old-location: tapi3\ittapi_get_callhubs.htm
tech.root: tapi3
ms.assetid: 57177526-1351-4f59-8f24-74d8b87d27c0
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],get_CallHubs method, ITTAPI.get_CallHubs, ITTAPI::get_CallHubs, _tapi3_ittapi_get_callhubs, get_CallHubs, get_CallHubs method [TAPI 2.2], get_CallHubs method [TAPI 2.2],ITTAPI interface, tapi3.ittapi_get_callhubs, tapi3if/ITTAPI::get_CallHubs
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
 - ITTAPI::get_CallHubs
 - tapi3if/ITTAPI::get_CallHubs
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
 - ITTAPI.get_CallHubs
---

# ITTAPI::get_CallHubs


## -description

The 
<b>get_CallHubs</b> method creates a collection of the currently available call hubs. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumeratecallhubs">EnumerateCallHubs</a> method.

## -parameters

### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> interface pointers (CallHub objects).

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not valid.

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
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>Addref</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> interface returned by <b>ITTAPI::get_CallHubs</b>. The application must call <b>Release</b> on the 
<b>ITCallHub</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>