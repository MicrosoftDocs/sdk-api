---
UID: NN:bits3_0.IBitsPeer
title: IBitsPeer
author: windows-sdk-content
description: Use IBitsPeer to get information about a peer in the neighborhood.
old-location: bits\ibitspeer.htm
old-project: Bits
ms.assetid: 617b88d4-6c3e-4c33-9bfa-6d9f6f629866
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IBitsPeer, IBitsPeer interface [BITS], IBitsPeer interface [BITS],described, bits.ibitspeer, bits3_0/IBitsPeer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bits.lib
-	Bits.dll
api_name:
-	IBitsPeer
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: BitsPrx4.dll
req.irql: 
---

# IBitsPeer interface


## -description


Use <b>IBitsPeer</b> to get information about a peer in the neighborhood. 

To get this  interface, call the <a href="https://msdn.microsoft.com/b5bc254d-d74e-4076-a22a-93abf9023068">IEnumBitsPeers::Next</a> method. 
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBitsPeer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBitsPeer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/71cfc0a5-1f60-4e61-a706-bb9f9c5a6c76">GetPeerName</a>
</td>
<td align="left" width="63%">
Gets the server principal name that uniquely identifies the peer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64718331-32a9-40ba-90f2-9dd9d8fea3e4">IsAuthenticated</a>
</td>
<td align="left" width="63%">
Determines whether the peer is authenticated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e38166da-2139-4108-bb8a-74bb7a7997c1">IsAvailable</a>
</td>
<td align="left" width="63%">
Determines whether the peer is available (online) to serve content.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5fa30b4e-f13c-4341-af65-a2e3d2703b96">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/2715a58c-ba76-4223-ad9e-453d029e0eda">IEnumBitsPeers</a>
 

 

