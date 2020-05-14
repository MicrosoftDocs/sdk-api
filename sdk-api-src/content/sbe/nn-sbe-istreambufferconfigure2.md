---
UID: NN:sbe.IStreamBufferConfigure2
title: IStreamBufferConfigure2 (sbe.h)
description: The IStreamBufferConfigure2 interface is exposed by the StreamBufferConfig object.helpviewer_keywords: ["IStreamBufferConfigure2","IStreamBufferConfigure2 interface [Microsoft TV Technologies]","IStreamBufferConfigure2 interface [Microsoft TV Technologies]","described","IStreamBufferConfigure2Interface","mstv.istreambufferconfigure2","sbe/IStreamBufferConfigure2"]
old-location: mstv\istreambufferconfigure2.htm
tech.root: mstv
ms.assetid: df71783c-1ff3-46b0-bae2-61d12f4d70d0
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure2, IStreamBufferConfigure2 interface [Microsoft TV Technologies], IStreamBufferConfigure2 interface [Microsoft TV Technologies],described, IStreamBufferConfigure2Interface, mstv.istreambufferconfigure2, sbe/IStreamBufferConfigure2
f1_keywords:
- sbe/IStreamBufferConfigure2
dev_langs:
- c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
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
- Sbe.h
api_name:
- IStreamBufferConfigure2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferConfigure2 interface


## -description



The <b>IStreamBufferConfigure2</b> interface is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/streambufferconfig-object">StreamBufferConfig</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferConfigure2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure">IStreamBufferConfigure</a>. <b>IStreamBufferConfigure2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferConfigure2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure2-getfftransitionrates">GetFFTransitionRates</a>
</td>
<td align="left" width="63%">
Returns the maximum full-frame and key-frame playback rates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure2-getmultiplexedpacketsize">GetMultiplexedPacketSize</a>
</td>
<td align="left" width="63%">
Returns the size of the multiplexed packets in the backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure2-setfftransitionrates">SetFFTransitionRates</a>
</td>
<td align="left" width="63%">
Sets the behavior of fast-forward play ("trick mode").

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure2-setmultiplexedpacketsize">SetMultiplexedPacketSize</a>
</td>
<td align="left" width="63%">
Sets the size of the multiplexed packets in the backing files.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferConfigure2)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure">IStreamBufferConfigure</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
 

 

