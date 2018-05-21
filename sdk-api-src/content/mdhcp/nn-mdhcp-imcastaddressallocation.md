---
UID: NN:mdhcp.IMcastAddressAllocation
title: IMcastAddressAllocation
author: windows-driver-content
description: IMcastAddressAllocation is the main interface for multicast address allocation. An application calls the COM CoCreateInstance function on this interface to create the multicast client interface object.
old-location: tapi3\imcastaddressallocation.htm
old-project: Tapi
ms.assetid: 359e67bb-9a5b-4caa-8d3b-eb0739b0828f
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IMcastAddressAllocation, IMcastAddressAllocation interface [TAPI 2.2], IMcastAddressAllocation interface [TAPI 2.2],described, _tapi3_imcastaddressallocation, mdhcp/IMcastAddressAllocation, tapi3.imcastaddressallocation
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MODEMSETTINGS, *PMODEMSETTINGS, *LPMODEMSETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mdhcp.dll
api_name:
-	IMcastAddressAllocation
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMcastAddressAllocation interface


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

<b>IMcastAddressAllocation</b> is the main interface for multicast address allocation. An application calls the COM 
<a href="_com_cocreateinstance">CoCreateInstance</a> function on this interface to create the multicast client interface object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMcastAddressAllocation</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMcastAddressAllocation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b7a65998-3329-4117-be91-10e2dd7047d5">CreateLeaseInfo</a>
</td>
<td align="left" width="63%">
Creates a lease information object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6390b21-348a-4bb9-8d21-3c585672199d">CreateLeaseInfoFromVariant</a>
</td>
<td align="left" width="63%">
Creates a lease information object. Similar to 
<a href="https://msdn.microsoft.com/b7a65998-3329-4117-be91-10e2dd7047d5">CreateLeaseInfo</a>, but used by Automation client languages such as Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1845f5f9-be0e-4609-89d8-1a0ed194dd68">EnumerateScopes</a>
</td>
<td align="left" width="63%">
Creates an enumeration of multicast scopes interfaces available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fe824fa-2fcb-4f6b-b3de-15dcfc79575c">get_Scopes</a>
</td>
<td align="left" width="63%">
Gets a <b>VARIANT</b> collection of 
<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a> pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b5fd18b-1b13-4e2a-9ff9-4a66212213a7">ReleaseAddress</a>
</td>
<td align="left" width="63%">
Releases a lease that was obtained previously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f52d1e9-61d9-4f67-b180-c1844b4eb7f1">RenewAddress</a>
</td>
<td align="left" width="63%">
Renews an address lease.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca428138-34d2-499d-9560-8dfd51403ba1">RequestAddress</a>
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




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/a4ad8009-559e-4db9-9ae2-28e4d36cf346">IMcastLeaseInfo</a>



<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a>
 

 

