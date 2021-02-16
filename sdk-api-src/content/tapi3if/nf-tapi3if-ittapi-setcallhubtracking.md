---
UID: NF:tapi3if.ITTAPI.SetCallHubTracking
title: ITTAPI::SetCallHubTracking (tapi3if.h)
description: The SetCallHubTracking method enables or disables CallHub tracking.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","SetCallHubTracking method","ITTAPI.SetCallHubTracking","ITTAPI::SetCallHubTracking","SetCallHubTracking","SetCallHubTracking method [TAPI 2.2]","SetCallHubTracking method [TAPI 2.2]","ITTAPI interface","_tapi3_ittapi_setcallhubtracking","tapi3.ittapi_setcallhubtracking","tapi3if/ITTAPI::SetCallHubTracking"]
old-location: tapi3\ittapi_setcallhubtracking.htm
tech.root: tapi3
ms.assetid: 8c33a294-ed45-4353-91ed-fa0d3d66e5da
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],SetCallHubTracking method, ITTAPI.SetCallHubTracking, ITTAPI::SetCallHubTracking, SetCallHubTracking, SetCallHubTracking method [TAPI 2.2], SetCallHubTracking method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_setcallhubtracking, tapi3.ittapi_setcallhubtracking, tapi3if/ITTAPI::SetCallHubTracking
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
 - ITTAPI::SetCallHubTracking
 - tapi3if/ITTAPI::SetCallHubTracking
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
 - ITTAPI.SetCallHubTracking
---

# ITTAPI::SetCallHubTracking


## -description

The 
<b>SetCallHubTracking</b> method enables or disables CallHub tracking.

## -parameters

### -param pAddresses [in]

Pointer to a <b>VARIANT</b> containing a <b>SAFEARRAY</b> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface pointers.

### -param bTracking [in]

VARIANT_TRUE to enable tracking, VARIANT_FALSE to disable.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>