---
UID: NF:msp.ITMSPAddress.CreateMSPCall
title: ITMSPAddress::CreateMSPCall (msp.h)
description: The ITMSPAddress::CreateMSPCall (msp.h) method creates an MSP Call object.
helpviewer_keywords: ["CreateMSPCall","CreateMSPCall method [TAPI 2.2]","CreateMSPCall method [TAPI 2.2]","ITMSPAddress interface","ITMSPAddress interface [TAPI 2.2]","CreateMSPCall method","ITMSPAddress.CreateMSPCall","ITMSPAddress::CreateMSPCall","_tapi3_itmspaddress_createmspcall","msp/ITMSPAddress::CreateMSPCall","tapi3.itmspaddress_createmspcall"]
old-location: tapi3\itmspaddress_createmspcall.htm
tech.root: tapi3
ms.assetid: 56ed10e3-e711-43ae-aad6-65a5992fca0f
ms.date: 08/08/2022
ms.keywords: CreateMSPCall, CreateMSPCall method [TAPI 2.2], CreateMSPCall method [TAPI 2.2],ITMSPAddress interface, ITMSPAddress interface [TAPI 2.2],CreateMSPCall method, ITMSPAddress.CreateMSPCall, ITMSPAddress::CreateMSPCall, _tapi3_itmspaddress_createmspcall, msp/ITMSPAddress::CreateMSPCall, tapi3.itmspaddress_createmspcall
req.header: msp.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITMSPAddress::CreateMSPCall
 - msp/ITMSPAddress::CreateMSPCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msp.h
api_name:
 - ITMSPAddress.CreateMSPCall
---

# ITMSPAddress::CreateMSPCall


## -description

The <b>CreateMSPCall</b> method creates an MSP Call object. TAPI aggregates this onto the main Call object and exposes the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a> interface.

## -parameters

### -param hCall [in]

Handle for this MSP.

### -param dwReserved [in]

Reserved value – will be 0.

### -param dwMediaType [in]

Indicates 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media types</a> required for the call.

### -param pOuterUnknown [in]

The pointer to the 
<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the TAPI 3 call object. Since the MSP Call object is aggregated in the TAPI 3 call object, it needs to know the outer <b>IUnknown</b>.

### -param ppStreamControl [out]

Pointer to <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a> interface for newly created call.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The MSP failed to initialize.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pMSPCallback</i> is not a valid pointer.

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
<dt><b>TAPI_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
<i>dwMediaType</i> is not a valid 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msp/nn-msp-itmspaddress">ITMSPAddress</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
