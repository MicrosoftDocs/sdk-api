---
UID: NN:strmif.IAMLatency
title: IAMLatency (strmif.h)

description: The IAMLatency interface reports the amount of latency that a filter introduces into the graph.
old-location: dshow\iamlatency.htm
tech.root: DirectShow
ms.assetid: 83384ef6-40d6-4d37-866d-6059dc5d7542

ms.date: 12/05/2018
ms.keywords: IAMLatency, IAMLatency interface [DirectShow], IAMLatency interface [DirectShow],described, IAMLatencyInterface, dshow.iamlatency, strmif/IAMLatency
ms.topic: interface
f1_keywords: 
 - "strmif/IAMLatency"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMLatency
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMLatency interface


## -description



The <code>IAMLatency</code> interface reports the amount of latency that a filter introduces into the graph. Latency is defined as the time that it takes the filter to process a sample. For a source filter, latency is the filter's maximum buffer size, measured in time. For example, a video capture filter that buffers one frame at 30 frames per second introduces a latency of about 33 milliseconds.

Currently, there is no support for using this interface by itself. A source filter that streams live or real-time data should implement the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource</a> interface, which inherits from this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMLatency</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMLatency</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMLatency</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamlatency-getlatency">GetLatency</a>
</td>
<td align="left" width="63%">
Retrieves the expected latency associated with this filter.

</td>
</tr>
</table> 

