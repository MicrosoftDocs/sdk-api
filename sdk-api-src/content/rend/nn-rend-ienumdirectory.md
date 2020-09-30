---
UID: NN:rend.IEnumDirectory
title: IEnumDirectory (rend.h)
description: The IEnumDirectory interface provides COM-standard enumeration methods for the ITDirectory interface. The ITRendezvous::EnumerateDefaultDirectories method returns a pointer to IEnumDirectory.
helpviewer_keywords: ["IEnumDirectory","IEnumDirectory interface [TAPI 2.2]","IEnumDirectory interface [TAPI 2.2]","described","_tapi3_ienumdirectory","rend/IEnumDirectory","tapi3.ienumdirectory"]
old-location: tapi3\ienumdirectory.htm
tech.root: tapi3
ms.assetid: 9c1e83c5-c718-4a3b-916d-e844a8377a29
ms.date: 12/05/2018
ms.keywords: IEnumDirectory, IEnumDirectory interface [TAPI 2.2], IEnumDirectory interface [TAPI 2.2],described, _tapi3_ienumdirectory, rend/IEnumDirectory, tapi3.ienumdirectory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumDirectory
 - rend/IEnumDirectory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - IEnumDirectory
---

# IEnumDirectory interface


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IEnumDirectory</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a> interface. The 
<a href="/windows/desktop/api/rend/nf-rend-itrendezvous-enumeratedefaultdirectories">ITRendezvous::EnumerateDefaultDirectories</a> method returns a pointer to 
<b>IEnumDirectory</b>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDirectory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumDirectory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumDirectory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rend/nf-rend-ienumdirectory-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rend/nf-rend-ienumdirectory-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rend/nf-rend-ienumdirectory-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rend/nf-rend-ienumdirectory-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table>