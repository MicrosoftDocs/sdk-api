---
UID: NF:tapi3if.ITAddress.CreateForwardInfoObject
title: ITAddress::CreateForwardInfoObject (tapi3if.h)
description: The CreateForwardInfoObject method creates the forwarding information object and returns an ITForwardInformation interface pointer.
helpviewer_keywords: ["CreateForwardInfoObject","CreateForwardInfoObject method [TAPI 2.2]","CreateForwardInfoObject method [TAPI 2.2]","ITAddress interface","ITAddress interface [TAPI 2.2]","CreateForwardInfoObject method","ITAddress.CreateForwardInfoObject","ITAddress::CreateForwardInfoObject","_tapi3_itaddress_createforwardinfoobject","tapi3.itaddress_createforwardinfoobject","tapi3if/ITAddress::CreateForwardInfoObject"]
old-location: tapi3\itaddress_createforwardinfoobject.htm
tech.root: tapi3
ms.assetid: 87d37ba3-5398-47a7-808b-eb9b6681653d
ms.date: 12/05/2018
ms.keywords: CreateForwardInfoObject, CreateForwardInfoObject method [TAPI 2.2], CreateForwardInfoObject method [TAPI 2.2],ITAddress interface, ITAddress interface [TAPI 2.2],CreateForwardInfoObject method, ITAddress.CreateForwardInfoObject, ITAddress::CreateForwardInfoObject, _tapi3_itaddress_createforwardinfoobject, tapi3.itaddress_createforwardinfoobject, tapi3if/ITAddress::CreateForwardInfoObject
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
 - ITAddress::CreateForwardInfoObject
 - tapi3if/ITAddress::CreateForwardInfoObject
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
 - ITAddress.CreateForwardInfoObject
---

# ITAddress::CreateForwardInfoObject


## -description

The 
<b>CreateForwardInfoObject</b> method creates the forwarding information object and returns an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a> interface pointer. This interface exposes methods that allow an application to control aspects of how a call is forwarded, such as whether internal calls will be handled differently than external calls.

## -parameters

### -param ppForwardInfo [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a> interface.

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
The <i>ppForwardInfo</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

The application must set information on a newly created 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a> object before the object can be used.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a> interface returned by <b>ITAddress::CreateForwardInfoObject</b>. The application must call <b>Release</b> on the 
<b>ITForwardInformation</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">Forward</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">get_CurrentForwardInfo</a>