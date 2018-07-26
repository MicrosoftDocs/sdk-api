---
UID: NN:mdhcp.IMcastScope
title: IMcastScope
author: windows-sdk-content
description: The IMcastScope interface is obtained by calling IMcastAddressAllocation::EnumerateScopes or IMcastAddressAllocation::get_Scopes.
old-location: tapi3\imcastscope.htm
old-project: tapi
ms.assetid: b0252ac4-856e-4aa7-aa3b-37b92472e864
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMcastScope, IMcastScope interface [TAPI 2.2], IMcastScope interface [TAPI 2.2],described, _tapi3_imcastscope, mdhcp/IMcastScope, tapi3.imcastscope
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
 - IMcastScope
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMcastScope interface


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IMcastScope</b> interface is obtained by calling 
<a href="https://msdn.microsoft.com/1845f5f9-be0e-4609-89d8-1a0ed194dd68">IMcastAddressAllocation::EnumerateScopes</a> or 
<a href="https://msdn.microsoft.com/4fe824fa-2fcb-4f6b-b3de-15dcfc79575c">IMcastAddressAllocation::get_Scopes</a>. It encapsulates all the properties of a multicast scope and provides methods to get information about the scope. This is a "read-only" interface in that it has "get" methods but no "put" methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMcastScope</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMcastScope</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/376ccbe4-ad83-4eef-88bd-11ed95d14359">get_InterfaceID</a>
</td>
<td align="left" width="63%">
Obtains the interface ID associated with this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e675ba4a-8e5f-42a6-8edf-9b136cf9dd46">get_ScopeDescription</a>
</td>
<td align="left" width="63%">
Obtains a textual description associated with this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c0ba8ab-1022-40c6-9d89-74250c149681">get_ScopeID</a>
</td>
<td align="left" width="63%">
Obtains the scope ID associated with this scope

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80c0ecca-647f-4e5e-92d6-fc95368715ad">get_ServerID</a>
</td>
<td align="left" width="63%">
Obtains the server ID associated with this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68e402e5-87ae-49fd-9149-8eb79a0a8aee">get_TTL</a>
</td>
<td align="left" width="63%">
Obtains time to live information for the multicast server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/a4ad8009-559e-4db9-9ae2-28e4d36cf346">IMcastLeaseInfo</a>
 

 

