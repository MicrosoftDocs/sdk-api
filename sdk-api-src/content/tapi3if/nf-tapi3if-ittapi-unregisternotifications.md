---
UID: NF:tapi3if.ITTAPI.UnregisterNotifications
title: ITTAPI::UnregisterNotifications (tapi3if.h)
description: The UnregisterNotifications method removes any incoming call notification registrations that have been performed using ITTAPI::RegisterCallNotifications.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","UnregisterNotifications method","ITTAPI.UnregisterNotifications","ITTAPI::UnregisterNotifications","UnregisterNotifications","UnregisterNotifications method [TAPI 2.2]","UnregisterNotifications method [TAPI 2.2]","ITTAPI interface","_tapi3_ittapi_unregisternotifications","tapi3.ittapi_unregisternotifications","tapi3if/ITTAPI::UnregisterNotifications"]
old-location: tapi3\ittapi_unregisternotifications.htm
tech.root: tapi3
ms.assetid: 66717165-1c29-4d77-b6ac-8c3638fb11f4
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],UnregisterNotifications method, ITTAPI.UnregisterNotifications, ITTAPI::UnregisterNotifications, UnregisterNotifications, UnregisterNotifications method [TAPI 2.2], UnregisterNotifications method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_unregisternotifications, tapi3.ittapi_unregisternotifications, tapi3if/ITTAPI::UnregisterNotifications
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
 - ITTAPI::UnregisterNotifications
 - tapi3if/ITTAPI::UnregisterNotifications
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
 - ITTAPI.UnregisterNotifications
---

# ITTAPI::UnregisterNotifications


## -description

The 
<b>UnregisterNotifications</b> method removes any incoming call notification registrations that have been performed using 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>.

## -parameters

### -param lRegister [in]

The value returned by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">RegisterCallNotifications</a> method in the <i>plRegister</i> parameter.

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
The TAPI object has not yet been initialized or the <i>lRegister</i> parameter is not valid.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">RegisterCallNotifications</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>