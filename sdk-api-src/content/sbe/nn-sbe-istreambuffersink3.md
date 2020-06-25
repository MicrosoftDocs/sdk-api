---
UID: NN:sbe.IStreamBufferSink3
title: IStreamBufferSink3 (sbe.h)
description: The IStreamBufferSink3 interface is exposed by the Stream Buffer Sink filter.
helpviewer_keywords: ["IStreamBufferSink3","IStreamBufferSink3 interface [Microsoft TV Technologies]","IStreamBufferSink3 interface [Microsoft TV Technologies]","described","IStreamBufferSink3Interface","mstv.istreambuffersink3","sbe/IStreamBufferSink3"]
old-location: mstv\istreambuffersink3.htm
tech.root: mstv
ms.assetid: a3adbe79-7d7c-4b12-a574-23c64d2311af
ms.date: 12/05/2018
ms.keywords: IStreamBufferSink3, IStreamBufferSink3 interface [Microsoft TV Technologies], IStreamBufferSink3 interface [Microsoft TV Technologies],described, IStreamBufferSink3Interface, mstv.istreambuffersink3, sbe/IStreamBufferSink3
f1_keywords:
- sbe/IStreamBufferSink3
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
- IStreamBufferSink3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferSink3 interface


## -description



The <b>IStreamBufferSink3</b> interface is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferSink3</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffersink2">IStreamBufferSink2</a>. <b>IStreamBufferSink3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferSink3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink3-setavailablefilter">SetAvailableFilter</a>
</td>
<td align="left" width="63%">
Limits how far the Stream Buffer Source filter can seek backward.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferSink3)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffersink2">IStreamBufferSink2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
 

 

