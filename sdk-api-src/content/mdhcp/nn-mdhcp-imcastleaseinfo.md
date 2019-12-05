---
UID: NN:mdhcp.IMcastLeaseInfo
title: IMcastLeaseInfo (mdhcp.h)
description: The IMcastLeaseInfo interface exposes methods that can get or set information concerning a multicast address allocation. The IMcastLease object is created by calling IMcastAddressAllocation::CreateLeaseInfo.
old-location: tapi3\imcastleaseinfo.htm
tech.root: Tapi
ms.assetid: a4ad8009-559e-4db9-9ae2-28e4d36cf346
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo, IMcastLeaseInfo interface [TAPI 2.2], IMcastLeaseInfo interface [TAPI 2.2],described, _tapi3_imcastleaseinfo, mdhcp/IMcastLeaseInfo, tapi3.imcastleaseinfo
ms.topic: interface
f1_keywords:
- mdhcp/IMcastLeaseInfo
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mdhcp.dll
api_name:
- IMcastLeaseInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMcastLeaseInfo interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IMcastLeaseInfo</b> interface exposes methods that can get or set information concerning a multicast address allocation. The IMcastLease object is created by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">IMcastAddressAllocation::CreateLeaseInfo</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMcastLeaseInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMcastLeaseInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMcastLeaseInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses">EnumerateAddresses</a>
</td>
<td align="left" width="63%">
Obtains the collection of multicast addresses that are the subject of this lease or lease request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-get_addresscount">get_AddressCount</a>
</td>
<td align="left" width="63%">
Obtains the number of addresses requested or granted in this lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-get_addresses">get_Addresses</a>
</td>
<td align="left" width="63%">
Obtains the collection of multicast addresses that are the subject of this lease or lease request. Similar to 
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses">EnumerateAddresses</a>, but used by scripting languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-get_leasestarttime">get_LeaseStartTime</a>
</td>
<td align="left" width="63%">
Obtains the start time of the lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-get_leasestoptime">get_LeaseStopTime</a>
</td>
<td align="left" width="63%">
Obtains the stop time of the lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-get_requestid">get_RequestID</a>
</td>
<td align="left" width="63%">
Obtains the request identifier of the lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-get_serveraddress">get_ServerAddress</a>
</td>
<td align="left" width="63%">
Obtains a string representing the address of the multicast server granting this lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-get_ttl">get_TTL</a>
</td>
<td align="left" width="63%">
Obtains the 
<a href="/windows/win32/tapi/t-tapgloss">TTL</a> (time to live) value associated with this lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-put_leasestarttime">put_LeaseStartTime</a>
</td>
<td align="left" width="63%">
Sets the start time of the lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-put_leasestoptime">put_LeaseStopTime</a>
</td>
<td align="left" width="63%">
Sets the stop time of the lease.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nn-mdhcp-imcastaddressallocation">IMcastAddressAllocation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">IMcastAddressAllocation::CreateLeaseInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-renewaddress">IMcastAddressAllocation::RenewAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress">IMcastAddressAllocation::RequestAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a>
 

 

