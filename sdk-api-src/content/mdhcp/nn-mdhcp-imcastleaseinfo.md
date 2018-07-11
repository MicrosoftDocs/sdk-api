---
UID: NN:mdhcp.IMcastLeaseInfo
title: IMcastLeaseInfo
author: windows-sdk-content
description: The IMcastLeaseInfo interface exposes methods that can get or set information concerning a multicast address allocation. The IMcastLease object is created by calling IMcastAddressAllocation::CreateLeaseInfo.
old-location: tapi3\imcastleaseinfo.htm
old-project: tapi
ms.assetid: a4ad8009-559e-4db9-9ae2-28e4d36cf346
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: IMcastLeaseInfo, IMcastLeaseInfo interface [TAPI 2.2], IMcastLeaseInfo interface [TAPI 2.2],described, _tapi3_imcastleaseinfo, mdhcp/IMcastLeaseInfo, tapi3.imcastleaseinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: MODEMSETTINGS, *PMODEMSETTINGS, *LPMODEMSETTINGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IMcastLeaseInfo
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMcastLeaseInfo interface


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IMcastLeaseInfo</b> interface exposes methods that can get or set information concerning a multicast address allocation. The IMcastLease object is created by calling 
<a href="https://msdn.microsoft.com/b7a65998-3329-4117-be91-10e2dd7047d5">IMcastAddressAllocation::CreateLeaseInfo</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMcastLeaseInfo</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMcastLeaseInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/edbfe386-9b3d-4160-916e-6c9ea640cfbc">EnumerateAddresses</a>
</td>
<td align="left" width="63%">
Obtains the collection of multicast addresses that are the subject of this lease or lease request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af7c6923-3859-46c0-aced-5b334a423e03">get_AddressCount</a>
</td>
<td align="left" width="63%">
Obtains the number of addresses requested or granted in this lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37dc1bc8-b3d9-4c84-8d37-89d50570d95c">get_Addresses</a>
</td>
<td align="left" width="63%">
Obtains the collection of multicast addresses that are the subject of this lease or lease request. Similar to 
<a href="https://msdn.microsoft.com/edbfe386-9b3d-4160-916e-6c9ea640cfbc">EnumerateAddresses</a>, but used by scripting languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0998a2d-6ec5-4d39-ba75-ede352b4cbe8">get_LeaseStartTime</a>
</td>
<td align="left" width="63%">
Obtains the start time of the lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2b99329-b176-4e5d-afb1-754c418e843a">get_LeaseStopTime</a>
</td>
<td align="left" width="63%">
Obtains the stop time of the lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/832bf532-4779-4066-a630-9892ad746a6c">get_RequestID</a>
</td>
<td align="left" width="63%">
Obtains the request identifier of the lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15f33689-07d5-4bd9-978a-2b5d9088b2ed">get_ServerAddress</a>
</td>
<td align="left" width="63%">
Obtains a string representing the address of the multicast server granting this lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/393b9d6c-430c-42f8-88fa-4bf5c9c04c1f">get_TTL</a>
</td>
<td align="left" width="63%">
Obtains the 
<a href="../tapi2/t_tapgloss.htm">TTL</a> (time to live) value associated with this lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f101a92a-bcbb-4d96-befd-c6ee83b68481">put_LeaseStartTime</a>
</td>
<td align="left" width="63%">
Sets the start time of the lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd171ebe-c436-46cf-9a4a-31f22acbaab2">put_LeaseStopTime</a>
</td>
<td align="left" width="63%">
Sets the stop time of the lease.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/359e67bb-9a5b-4caa-8d3b-eb0739b0828f">IMcastAddressAllocation</a>



<a href="https://msdn.microsoft.com/b7a65998-3329-4117-be91-10e2dd7047d5">IMcastAddressAllocation::CreateLeaseInfo</a>



<a href="https://msdn.microsoft.com/9f52d1e9-61d9-4f67-b180-c1844b4eb7f1">IMcastAddressAllocation::RenewAddress</a>



<a href="https://msdn.microsoft.com/ca428138-34d2-499d-9560-8dfd51403ba1">IMcastAddressAllocation::RequestAddress</a>



<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a>
 

 

