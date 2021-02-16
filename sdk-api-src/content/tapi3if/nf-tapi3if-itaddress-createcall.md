---
UID: NF:tapi3if.ITAddress.CreateCall
title: ITAddress::CreateCall (tapi3if.h)
description: The CreateCall method creates a new Call object that can be used to make an outgoing call and returns a pointer to the object's ITBasicCallControl interface. The newly created call is in the CS_IDLE state and has no media or terminals selected.
helpviewer_keywords: ["CreateCall","CreateCall method [TAPI 2.2]","CreateCall method [TAPI 2.2]","ITAddress interface","ITAddress interface [TAPI 2.2]","CreateCall method","ITAddress.CreateCall","ITAddress::CreateCall","_tapi3_itaddress_createcall","tapi3.itaddress_createcall","tapi3if/ITAddress::CreateCall"]
old-location: tapi3\itaddress_createcall.htm
tech.root: tapi3
ms.assetid: 1b5a755c-fdaf-42ca-9747-9b34efbd0ac3
ms.date: 12/05/2018
ms.keywords: CreateCall, CreateCall method [TAPI 2.2], CreateCall method [TAPI 2.2],ITAddress interface, ITAddress interface [TAPI 2.2],CreateCall method, ITAddress.CreateCall, ITAddress::CreateCall, _tapi3_itaddress_createcall, tapi3.itaddress_createcall, tapi3if/ITAddress::CreateCall
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
 - ITAddress::CreateCall
 - tapi3if/ITAddress::CreateCall
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
 - ITAddress.CreateCall
---

# ITAddress::CreateCall


## -description

The 
<b>CreateCall</b> method creates a new Call object that can be used to make an outgoing call and returns a pointer to the object's 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a> interface. The newly created call is in the CS_IDLE 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">state</a> and has no media or terminals selected.

Acceptable input values for call address, address type, and media types are specific to the telephony service provider that supports the current address. For information on TSPs shipped with Windows 2000, see 
<a href="/windows/desktop/Tapi/about-the-telephony-service-provider-tsp-">About The Telephony Service Provider (TSP)</a>. For third party TSPs, see the documentation provided by the vender.

## -parameters

### -param pDestAddress [in]

This <b>BSTR</b> string contains a destination address. The format is provider-specific. This pointer can be <b>NULL</b> for non-dialed addresses (such as with a hot phone) or when all dialing is performed using 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial">ITBasicCallControl::Dial</a>. <b>NULL</b> in combination with a <b>NULL</b><i>pGroupID</i> in 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup">ITBasicCallControl::Pickup</a> results in a group pickup. Service providers that have inverse multiplexing capabilities can allow an application to specify multiple addresses at once.

### -param lAddressType [in]

Contains an 
<a href="/windows/desktop/Tapi/lineaddresstype--constants">address type</a> constant, such as LINEADDRESSTYPE_PHONENUMBER, which describes the format of the address. The value must be valid for this address. Use 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability">ITAddressCapabilities::get_AddressCapability</a> with <i>AddressCap</i> set to AC_ADDRESSTYPES to verify the value.

### -param lMediaTypes [in]

Identifies the 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> or types that will be involved in the call session.

### -param ppCall [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a> interface.

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
The address type, <i>lAddressType</i>, is invalid or specifies more than one address type.

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
The <i>ppCall</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDestAddress</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

When the address type is LINEADDRESSTYPE_SDP, the application should call the 
<a href="/windows/desktop/Tapi/itsdp-get-isvalid">ITSDP::get_IsValid</a> method on <i>pDestAddress</i> to verify that the SDP information contained is properly constructed according to RFC 2327.

Calls used as consultation calls, such as during a conference, transfer, or forward operation, must be created using this method.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a> interface returned by <b>ITAddress::CreateCall</b>. The application must call <b>Release</b> on the 
<b>ITBasicCallControl</b> interface to free resources associated with it.

<div class="alert"><b>Note</b>    This method is not precisely the same as 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> in TAPI 2. It supplies TAPI with much of the same information, but parallel operations are not performed until 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect">ITBasicCallControl::Connect</a> is called.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial">ITBasicCallControl::Dial</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a>