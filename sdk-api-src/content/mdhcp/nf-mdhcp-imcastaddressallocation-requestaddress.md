---
UID: NF:mdhcp.IMcastAddressAllocation.RequestAddress
title: IMcastAddressAllocation::RequestAddress (mdhcp.h)
description: The RequestAddress method obtains a new lease for one or more multicast addresses. The EnumerateScopes or get_Scopes method must be called first.
helpviewer_keywords: ["IMcastAddressAllocation interface [TAPI 2.2]","RequestAddress method","IMcastAddressAllocation.RequestAddress","IMcastAddressAllocation::RequestAddress","RequestAddress","RequestAddress method [TAPI 2.2]","RequestAddress method [TAPI 2.2]","IMcastAddressAllocation interface","_tapi3_imcastaddressallocation_requestaddress","mdhcp/IMcastAddressAllocation::RequestAddress","tapi3.imcastaddressallocation_requestaddress"]
old-location: tapi3\imcastaddressallocation_requestaddress.htm
tech.root: tapi3
ms.assetid: ca428138-34d2-499d-9560-8dfd51403ba1
ms.date: 12/05/2018
ms.keywords: IMcastAddressAllocation interface [TAPI 2.2],RequestAddress method, IMcastAddressAllocation.RequestAddress, IMcastAddressAllocation::RequestAddress, RequestAddress, RequestAddress method [TAPI 2.2], RequestAddress method [TAPI 2.2],IMcastAddressAllocation interface, _tapi3_imcastaddressallocation_requestaddress, mdhcp/IMcastAddressAllocation::RequestAddress, tapi3.imcastaddressallocation_requestaddress
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
 - IMcastAddressAllocation::RequestAddress
 - mdhcp/IMcastAddressAllocation::RequestAddress
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
 - IMcastAddressAllocation.RequestAddress
---

# IMcastAddressAllocation::RequestAddress


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>RequestAddress</b> method obtains a new lease for one or more multicast addresses. The 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes">EnumerateScopes</a> or 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-get_scopes">get_Scopes</a> method must be called first.

## -parameters

### -param pScope [in]

Identifies the multicast scope from which the application needs an address. The application first calls 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-get_scopes">get_Scopes</a> or 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes">EnumerateScopes</a> to obtain a list of available scopes.

### -param LeaseStartTime [in]

Requested time for the lease on these addresses to start. The start time that is actually granted may be different.

### -param LeaseStopTime [in]

Requested time for the lease on these addresses to stop. The stop time that is actually granted may be different.

### -param NumAddresses [in]

The number of addresses requested. Fewer addresses may actually be granted.

### -param ppLeaseResponse [out]

Pointer to an interface pointer that will be set to point to a new 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a> object. This interface can then be used to discover the actual attributes of the granted lease. See 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a> for more information.

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
The caller passed in an invalid pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to create the required objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Requested stop time is prior to requested stop time.

</td>
</tr>
</table>

## -remarks

Although these COM interfaces and their implementation support allocation of multiple addresses at a time, multiple allocation is not currently supported by the underlying function calls. You may need to use a loop for multiple address allocation.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a> interface returned by <b>IMcastAddressAllocation::RequestAddress</b>. The application must call <b>Release</b> on the 
<b>IMcastLeaseInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastaddressallocation">IMcastAddressAllocation</a>