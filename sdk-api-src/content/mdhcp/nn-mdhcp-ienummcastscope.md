---
UID: NN:mdhcp.IEnumMcastScope
title: IEnumMcastScope (mdhcp.h)
description: The IEnumMcastScope interface provides COM-standard enumeration methods for the IMcastScope interface. The IMcastAddressAllocation::EnumerateScopes method returns a pointer to IEnumMcastScope.
helpviewer_keywords: ["IEnumMcastScope","IEnumMcastScope interface [TAPI 2.2]","IEnumMcastScope interface [TAPI 2.2]","described","_tapi3_ienummcastscope","mdhcp/IEnumMcastScope","tapi3.ienummcastscope"]
old-location: tapi3\ienummcastscope.htm
tech.root: Tapi
ms.assetid: edc8be8e-635b-43f3-a4c1-7566e354cc3e
ms.date: 12/05/2018
ms.keywords: IEnumMcastScope, IEnumMcastScope interface [TAPI 2.2], IEnumMcastScope interface [TAPI 2.2],described, _tapi3_ienummcastscope, mdhcp/IEnumMcastScope, tapi3.ienummcastscope
f1_keywords:
- mdhcp/IEnumMcastScope
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
- IEnumMcastScope
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumMcastScope interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IEnumMcastScope</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a> interface. The 
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes">IMcastAddressAllocation::EnumerateScopes</a> method returns a pointer to 
<b>IEnumMcastScope</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumMcastScope</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumMcastScope</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumMcastScope</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-ienummcastscope-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.</p> (Inherited from IEnumMcastScopes)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-ienummcastscope-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.</p> (Inherited from IEnumMcastScopes)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-ienummcastscope-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.</p> (Inherited from IEnumMcastScopes)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-ienummcastscope-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.</p> (Inherited from IEnumMcastScopes)</td>
</tr>
</table> 

