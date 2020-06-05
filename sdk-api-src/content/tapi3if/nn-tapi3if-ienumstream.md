---
UID: NN:tapi3if.IEnumStream
title: IEnumStream (tapi3if.h)
description: The IEnumStream interface provides COM-standard enumeration methods for the ITStream interface. The ITStreamControl::EnumerateStreams and ITParticipant::EnumerateStreams methods return a pointer to IEnumStream.helpviewer_keywords: ["IEnumStream","IEnumStream interface [TAPI 2.2]","IEnumStream interface [TAPI 2.2]","described","_tapi3_ienumstream","tapi3.ienumstream","tapi3if/IEnumStream"]
old-location: tapi3\ienumstream.htm
tech.root: Tapi
ms.assetid: 52e8c040-8bc5-4c9c-a697-ec05164adea2
ms.date: 12/05/2018
ms.keywords: IEnumStream, IEnumStream interface [TAPI 2.2], IEnumStream interface [TAPI 2.2],described, _tapi3_ienumstream, tapi3.ienumstream, tapi3if/IEnumStream
f1_keywords:
- tapi3if/IEnumStream
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
- IEnumStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumStream interface


## -description


The 
<b>IEnumStream</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-enumeratestreams">ITStreamControl::EnumerateStreams</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-enumeratestreams">ITParticipant::EnumerateStreams</a> methods return a pointer to 
<b>IEnumStream</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumstream-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumstream-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumstream-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to beginning of enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumstream-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
 

 

