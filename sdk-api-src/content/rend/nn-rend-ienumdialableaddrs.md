---
UID: NN:rend.IEnumDialableAddrs
title: IEnumDialableAddrs (rend.h)
description: The IEnumDialableAddrs interface provides COM-standard enumeration methods to discover and use the available dialable addresses in a directory. The ITDirectoryObject::EnumerateDialableAddrs method returns a pointer to this interface.helpviewer_keywords: ["IEnumDialableAddrs","IEnumDialableAddrs interface [TAPI 2.2]","IEnumDialableAddrs interface [TAPI 2.2]","described","_tapi3_ienumdialableaddrs","rend/IEnumDialableAddrs","tapi3.ienumdialableaddrs"]
old-location: tapi3\ienumdialableaddrs.htm
tech.root: Tapi
ms.assetid: 0a64cb89-9e44-4af1-9b0f-2eec6e5267c7
ms.date: 12/05/2018
ms.keywords: IEnumDialableAddrs, IEnumDialableAddrs interface [TAPI 2.2], IEnumDialableAddrs interface [TAPI 2.2],described, _tapi3_ienumdialableaddrs, rend/IEnumDialableAddrs, tapi3.ienumdialableaddrs
f1_keywords:
- rend/IEnumDialableAddrs
dev_langs:
- c++
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Rend.dll
api_name:
- IEnumDialableAddrs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumDialableAddrs interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IEnumDialableAddrs</b> interface provides COM-standard enumeration methods to discover and use the available dialable addresses in a directory. The 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobject-enumeratedialableaddrs">ITDirectoryObject::EnumerateDialableAddrs</a> method returns a pointer to this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDialableAddrs</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumDialableAddrs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumDialableAddrs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdialableaddrs-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdialableaddrs-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdialableaddrs-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdialableaddrs-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

