---
UID: NF:mdhcp.IMcastAddressAllocation.RenewAddress
title: IMcastAddressAllocation::RenewAddress (mdhcp.h)
description: The RenewAddress method renews an address lease. Call CreateLeaseInfo to specify the parameters of the renewal request, and then call this method to make the request.
helpviewer_keywords: ["IMcastAddressAllocation interface [TAPI 2.2]","RenewAddress method","IMcastAddressAllocation.RenewAddress","IMcastAddressAllocation::RenewAddress","RenewAddress","RenewAddress method [TAPI 2.2]","RenewAddress method [TAPI 2.2]","IMcastAddressAllocation interface","_tapi3_imcastaddressallocation_renewaddress","mdhcp/IMcastAddressAllocation::RenewAddress","tapi3.imcastaddressallocation_renewaddress"]
old-location: tapi3\imcastaddressallocation_renewaddress.htm
tech.root: tapi3
ms.assetid: 9f52d1e9-61d9-4f67-b180-c1844b4eb7f1
ms.date: 12/05/2018
ms.keywords: IMcastAddressAllocation interface [TAPI 2.2],RenewAddress method, IMcastAddressAllocation.RenewAddress, IMcastAddressAllocation::RenewAddress, RenewAddress, RenewAddress method [TAPI 2.2], RenewAddress method [TAPI 2.2],IMcastAddressAllocation interface, _tapi3_imcastaddressallocation_renewaddress, mdhcp/IMcastAddressAllocation::RenewAddress, tapi3.imcastaddressallocation_renewaddress
req.header: mdhcp.h
req.include-header: 
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
req.dll: Mdhcp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMcastAddressAllocation::RenewAddress
 - mdhcp/IMcastAddressAllocation::RenewAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IMcastAddressAllocation.RenewAddress
---

# IMcastAddressAllocation::RenewAddress


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>RenewAddress</b> method renews an address lease. Call 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">CreateLeaseInfo</a> to specify the parameters of the renewal request, and then call this method to make the request.

## -parameters

### -param lReserved [in]

Reserved parameter. An application should pass in a value of 0.

### -param pRenewRequest [in]

Pointer to an 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a> object specifying the attributes of the requested renewal, such as which address(es) to renew. This is obtained by calling 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">CreateLeaseInfo</a>.

### -param ppRenewResponse [out]

Pointer to an interface pointer that will be set to point to a new 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a> object. This interface can then be used to discover the attributes of the renewed lease. See 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a> for more information.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The caller passed in an invalid pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Requested stop time is prior to the requested stop time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to create the required objects.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastaddressallocation">IMcastAddressAllocation</a>