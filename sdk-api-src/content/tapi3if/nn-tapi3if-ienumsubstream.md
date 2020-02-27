---
UID: NN:tapi3if.IEnumSubStream
title: IEnumSubStream (tapi3if.h)
description: The IEnumSubStream interface provides COM-standard enumeration methods for the ITSubStream interface. The ITSubStreamControl::EnumerateSubStreams method returns a pointer to IEnumSubStream.
old-location: tapi3\ienumsubstream.htm
tech.root: Tapi
ms.assetid: d9076a32-983e-48d4-b025-5fc770156df6
ms.date: 12/05/2018
ms.keywords: IEnumSubStream, IEnumSubStream interface [TAPI 2.2], IEnumSubStream interface [TAPI 2.2],described, _tapi3_ienumsubstream, tapi3.ienumsubstream, tapi3if/IEnumSubStream
f1_keywords:
- tapi3if/IEnumSubStream
dev_langs:
- c++
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tapi3if.h
api_name:
- IEnumSubStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSubStream interface


## -description


The 
<b>IEnumSubStream</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a> interface. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itsubstreamcontrol-enumeratesubstreams">ITSubStreamControl::EnumerateSubStreams</a> method returns a pointer to 
<b>IEnumSubStream</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSubStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSubStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSubStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumsubstream-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumsubstream-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumsubstream-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to beginning of enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumsubstream-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
 

 

