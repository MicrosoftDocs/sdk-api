---
UID: NF:mdhcp.IMcastAddressAllocation.CreateLeaseInfo
title: IMcastAddressAllocation::CreateLeaseInfo (mdhcp.h)
description: The CreateLeaseInfo method creates a lease information object for a subsequent call to RenewAddress or ReleaseAddress.
helpviewer_keywords: ["CreateLeaseInfo","CreateLeaseInfo method [TAPI 2.2]","CreateLeaseInfo method [TAPI 2.2]","IMcastAddressAllocation interface","IMcastAddressAllocation interface [TAPI 2.2]","CreateLeaseInfo method","IMcastAddressAllocation.CreateLeaseInfo","IMcastAddressAllocation::CreateLeaseInfo","_tapi3_imcastaddressallocation_createleaseinfo","mdhcp/IMcastAddressAllocation::CreateLeaseInfo","tapi3.imcastaddressallocation_createleaseinfo"]
old-location: tapi3\imcastaddressallocation_createleaseinfo.htm
tech.root: tapi3
ms.assetid: b7a65998-3329-4117-be91-10e2dd7047d5
ms.date: 12/05/2018
ms.keywords: CreateLeaseInfo, CreateLeaseInfo method [TAPI 2.2], CreateLeaseInfo method [TAPI 2.2],IMcastAddressAllocation interface, IMcastAddressAllocation interface [TAPI 2.2],CreateLeaseInfo method, IMcastAddressAllocation.CreateLeaseInfo, IMcastAddressAllocation::CreateLeaseInfo, _tapi3_imcastaddressallocation_createleaseinfo, mdhcp/IMcastAddressAllocation::CreateLeaseInfo, tapi3.imcastaddressallocation_createleaseinfo
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
 - IMcastAddressAllocation::CreateLeaseInfo
 - mdhcp/IMcastAddressAllocation::CreateLeaseInfo
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
 - IMcastAddressAllocation.CreateLeaseInfo
---

# IMcastAddressAllocation::CreateLeaseInfo


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>CreateLeaseInfo</b> method creates a lease information object for a subsequent call to 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-renewaddress">RenewAddress</a> or 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-releaseaddress">ReleaseAddress</a>.

## -parameters

### -param LeaseStartTime [in]

The start time of the lease.

### -param LeaseStopTime [in]

The stop time of the lease.

### -param dwNumAddresses [in]

The number of addresses associated with the lease.

### -param ppAddresses [in]

An array of <b>LPWSTR</b> pointers of size <i>dwNumAddresses</i>. Each <b>LPWSTR</b> is an IP version 4 address in dotted quad notation (for example, 10.111.222.111).

### -param pRequestID [in]

An <b>LPWSTR</b> specifying the request ID for the original request. This is obtained by calling 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-get_requestid">IMcastLeaseInfo::get_RequestID</a> on the lease information object corresponding to the original request. The request ID should be saved in persistent storage between executions of the application program. If you are renewing or releasing a lease that was requested during the same run of the application, you have no reason to use 
<b>CreateLeaseInfo</b>; just pass the existing 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a> pointer to 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-renewaddress">RenewAddress</a> or 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-releaseaddress">ReleaseAddress</a>.

### -param pServerAddress [in]

Specifies server address.

### -param ppReleaseRequest [out]

Pointer to the 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a> interface created.

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
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a> interface returned by <b>IMcastAddressAllocation::CreateLeaseInfo</b>. The application must call <b>Release</b> on the 
<b>IMcastLeaseInfo</b> interface to free resources associated with it.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastaddressallocation">IMcastAddressAllocation</a>