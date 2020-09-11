---
UID: NN:mdhcp.IMcastAddressAllocation
title: IMcastAddressAllocation (mdhcp.h)
description: IMcastAddressAllocation is the main interface for multicast address allocation. An application calls the COM CoCreateInstance function on this interface to create the multicast client interface object.
helpviewer_keywords: ["IMcastAddressAllocation","IMcastAddressAllocation interface [TAPI 2.2]","IMcastAddressAllocation interface [TAPI 2.2]","described","_tapi3_imcastaddressallocation","mdhcp/IMcastAddressAllocation","tapi3.imcastaddressallocation"]
old-location: tapi3\imcastaddressallocation.htm
tech.root: tapi3
ms.assetid: 359e67bb-9a5b-4caa-8d3b-eb0739b0828f
ms.date: 12/05/2018
ms.keywords: IMcastAddressAllocation, IMcastAddressAllocation interface [TAPI 2.2], IMcastAddressAllocation interface [TAPI 2.2],described, _tapi3_imcastaddressallocation, mdhcp/IMcastAddressAllocation, tapi3.imcastaddressallocation
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
 - IMcastAddressAllocation
 - mdhcp/IMcastAddressAllocation
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
 - IMcastAddressAllocation
---

# IMcastAddressAllocation interface


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

<b>IMcastAddressAllocation</b> is the main interface for multicast address allocation. An application calls the COM 
<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function on this interface to create the multicast client interface object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMcastAddressAllocation</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMcastAddressAllocation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMcastAddressAllocation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">CreateLeaseInfo</a>
</td>
<td align="left" width="63%">
Creates a lease information object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfofromvariant">CreateLeaseInfoFromVariant</a>
</td>
<td align="left" width="63%">
Creates a lease information object. Similar to 
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">CreateLeaseInfo</a>, but used by Automation client languages such as Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes">EnumerateScopes</a>
</td>
<td align="left" width="63%">
Creates an enumeration of multicast scopes interfaces available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-get_scopes">get_Scopes</a>
</td>
<td align="left" width="63%">
Gets a <b>VARIANT</b> collection of 
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a> pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-releaseaddress">ReleaseAddress</a>
</td>
<td align="left" width="63%">
Releases a lease that was obtained previously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-renewaddress">RenewAddress</a>
</td>
<td align="left" width="63%">
Renews an address lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress">RequestAddress</a>
</td>
<td align="left" width="63%">
Obtains a new lease for one or more multicast addresses.

</td>
</tr>
</table>

## -remarks

The multicast COM interfaces allow access to the network's facility for allocating, renewing, and releasing leases on multicast addresses. They encapsulate a set of function and data structure definitions. The COM interfaces free the programmer from the burden of understanding and manipulating these data structures. Moreover, because TAPI 3 itself is COM-based, these interfaces make multicast address allocation accessible in a way that is consistent with the other facilities provided by TAPI 3. Applications written using Visual Basic, Java, or scripting languages must use these COM interfaces—they cannot normally access the Windows API directly.

In addition, this component provides seamless and transparent support for local address allocation for non-multicast environments. The <b>DWORD</b> registry value <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\MCAST\LocalAllocation</b>, when set to a nonzero value, specifies that random number generation performed on the local machine is to be used for the allocation of all multicast addresses. This allows applications to function the same way on a network without a multicast address allocation server as they would on a network with a multicast address allocation server. If the registry value is set to zero or does not exist, this component performs normally as described in the rest of this specification. Note that local address allocation is never used unless this registry key is set to a nonzero value; local address allocation is not a fallback mechanism for a temporarily inaccessible multicast address allocation server.

Multicast address allocation is currently the subject of an IETF working group. To access current information, query on "Internet draft" and "MDHCP" or "MADCAP" using any Internet search engine. In addition to MADCAP (previously called MDHCP), the proposed architecture includes a protocol for server-to-server coordination within a domain or AS, as well as a protocol for interdomain coordination. While this architecture is currently evolving, the client need not concern itself with the details of this scheme.

This component currently supports only IP version 4 addresses.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a>

