---
UID: NN:mdhcp.IMcastScope
title: IMcastScope (mdhcp.h)

description: The IMcastScope interface is obtained by calling IMcastAddressAllocation::EnumerateScopes or IMcastAddressAllocation::get_Scopes.
old-location: tapi3\imcastscope.htm
tech.root: Tapi
ms.assetid: b0252ac4-856e-4aa7-aa3b-37b92472e864

ms.date: 12/05/2018
ms.keywords: IMcastScope, IMcastScope interface [TAPI 2.2], IMcastScope interface [TAPI 2.2],described, _tapi3_imcastscope, mdhcp/IMcastScope, tapi3.imcastscope
ms.topic: interface
f1_keywords: 
 - "mdhcp/IMcastScope"
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
 - IMcastScope
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMcastScope interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IMcastScope</b> interface is obtained by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes">IMcastAddressAllocation::EnumerateScopes</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-get_scopes">IMcastAddressAllocation::get_Scopes</a>. It encapsulates all the properties of a multicast scope and provides methods to get information about the scope. This is a "read-only" interface in that it has "get" methods but no "put" methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMcastScope</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMcastScope</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMcastScope</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastscope-get_interfaceid">get_InterfaceID</a>
</td>
<td align="left" width="63%">
Obtains the interface ID associated with this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastscope-get_scopedescription">get_ScopeDescription</a>
</td>
<td align="left" width="63%">
Obtains a textual description associated with this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastscope-get_scopeid">get_ScopeID</a>
</td>
<td align="left" width="63%">
Obtains the scope ID associated with this scope

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastscope-get_serverid">get_ServerID</a>
</td>
<td align="left" width="63%">
Obtains the server ID associated with this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastscope-get_ttl">get_TTL</a>
</td>
<td align="left" width="63%">
Obtains time to live information for the multicast server.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>
 

 

