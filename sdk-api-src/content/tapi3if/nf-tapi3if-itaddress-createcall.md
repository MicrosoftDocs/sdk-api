---
UID: NF:tapi3if.ITAddress.CreateCall
title: ITAddress::CreateCall
author: windows-sdk-content
description: The CreateCall method creates a new Call object that can be used to make an outgoing call and returns a pointer to the object's ITBasicCallControl interface. The newly created call is in the CS_IDLE state and has no media or terminals selected.
old-location: tapi3\itaddress_createcall.htm
tech.root: tapi
ms.assetid: 1b5a755c-fdaf-42ca-9747-9b34efbd0ac3
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CreateCall, CreateCall method [TAPI 2.2], CreateCall method [TAPI 2.2],ITAddress interface, ITAddress interface [TAPI 2.2],CreateCall method, ITAddress.CreateCall, ITAddress::CreateCall, _tapi3_itaddress_createcall, tapi3.itaddress_createcall, tapi3if/ITAddress::CreateCall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddress.CreateCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress::CreateCall


## -description


The 
<b>CreateCall</b> method creates a new Call object that can be used to make an outgoing call and returns a pointer to the object's 
<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a> interface. The newly created call is in the CS_IDLE 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">state</a> and has no media or terminals selected.

Acceptable input values for call address, address type, and media types are specific to the telephony service provider that supports the current address. For information on TSPs shipped with Windows 2000, see 
<a href="https://msdn.microsoft.com/6e4fb295-940e-4f76-ad43-fad7da90094a">About The Telephony Service Provider (TSP)</a>. For third party TSPs, see the documentation provided by the vender.


## -parameters




### -param pDestAddress [in]

This <b>BSTR</b> string contains a destination address. The format is provider-specific. This pointer can be <b>NULL</b> for non-dialed addresses (such as with a hot phone) or when all dialing is performed using 
<a href="https://msdn.microsoft.com/31fea4d8-9028-48d5-9f5d-53f1451103c7">ITBasicCallControl::Dial</a>. <b>NULL</b> in combination with a <b>NULL</b><i>pGroupID</i> in 
<a href="https://msdn.microsoft.com/25da3cf2-50f0-4f64-94ce-cf952e057376">ITBasicCallControl::Pickup</a> results in a group pickup. Service providers that have inverse multiplexing capabilities can allow an application to specify multiple addresses at once.


### -param lAddressType [in]

Contains an 
<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">address type</a> constant, such as LINEADDRESSTYPE_PHONENUMBER, which describes the format of the address. The value must be valid for this address. Use 
<a href="https://msdn.microsoft.com/76e61d5e-48b6-4b9c-9076-bd20a794859c">ITAddressCapabilities::get_AddressCapability</a> with <i>AddressCap</i> set to AC_ADDRESSTYPES to verify the value.


### -param lMediaTypes [in]

Identifies the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> or types that will be involved in the call session.


### -param ppCall [out]

Pointer to 
<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a> interface.


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
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pDestAddress</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

When the address type is LINEADDRESSTYPE_SDP, the application should call the 
<a href="https://msdn.microsoft.com/a3f849ac-bda9-4937-bf3b-bce8df20cbf0">ITSDP::get_IsValid</a> method on <i>pDestAddress</i> to verify that the SDP information contained is properly constructed according to RFC 2327.

Calls used as consultation calls, such as during a conference, transfer, or forward operation, must be created using this method.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a> interface returned by <b>ITAddress::CreateCall</b>. The application must call <b>Release</b> on the 
<b>ITBasicCallControl</b> interface to free resources associated with it.

<div class="alert"><b>Note</b>    This method is not precisely the same as 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> in TAPI 2. It supplies TAPI with much of the same information, but parallel operations are not performed until 
<a href="https://msdn.microsoft.com/cc9a8bfd-14c0-459c-a911-325b73323c08">ITBasicCallControl::Connect</a> is called.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/31fea4d8-9028-48d5-9f5d-53f1451103c7">ITBasicCallControl::Dial</a>



<a href="https://msdn.microsoft.com/111e6c11-67a7-4aab-81dd-f1b4316887e7">lineDial</a>
 

 

