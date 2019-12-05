---
UID: NN:bits3_0.IBitsPeer
title: IBitsPeer (bits3_0.h)
description: Use IBitsPeer to get information about a peer in the neighborhood.
old-location: bits\ibitspeer.htm
tech.root: Bits
ms.assetid: 617b88d4-6c3e-4c33-9bfa-6d9f6f629866
ms.date: 12/05/2018
ms.keywords: IBitsPeer, IBitsPeer interface [BITS], IBitsPeer interface [BITS],described, bits.ibitspeer, bits3_0/IBitsPeer
ms.topic: interface
f1_keywords:
- bits3_0/IBitsPeer
dev_langs:
- c++
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Bits.lib
- Bits.dll
api_name:
- IBitsPeer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBitsPeer interface


## -description


Use <b>IBitsPeer</b> to get information about a peer in the neighborhood. 

To get this  interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ienumbitspeers-next">IEnumBitsPeers::Next</a> method. 
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBitsPeer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBitsPeer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBitsPeer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeer-getpeername">GetPeerName</a>
</td>
<td align="left" width="63%">
Gets the server principal name that uniquely identifies the peer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeer-isauthenticated">IsAuthenticated</a>
</td>
<td align="left" width="63%">
Determines whether the peer is authenticated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeer-isavailable">IsAvailable</a>
</td>
<td align="left" width="63%">
Determines whether the peer is available (online) to serve content.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeers">IEnumBitsPeers</a>
 

 

