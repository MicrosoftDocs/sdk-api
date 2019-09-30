---
UID: NN:strmif.IAMGraphStreams
title: IAMGraphStreams (strmif.h)
author: windows-sdk-content
description: The IAMGraphStreams interface controls a filter graph that renders a live source.
old-location: dshow\iamgraphstreams.htm
tech.root: DirectShow
ms.assetid: 30d44536-2a2d-44ab-bafc-bdb851cd272b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMGraphStreams, IAMGraphStreams interface [DirectShow], IAMGraphStreams interface [DirectShow],described, IAMGraphStreamsInterface, dshow.iamgraphstreams, strmif/IAMGraphStreams
ms.topic: interface
f1_keywords: 
 - "strmif/IAMGraphStreams"
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
 - IAMGraphStreams
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMGraphStreams interface


## -description



The <code>IAMGraphStreams</code> interface controls a filter graph that renders a live source. A live source is one that streams data in real time, such as a capture device or a network broadcast. The Filter Graph Manager implements this interface.

Applications can use this interface to specify how the graph handles latency and synchronization when it renders a live source. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/live-sources">Live Sources</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMGraphStreams</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMGraphStreams</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMGraphStreams</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamgraphstreams-findupstreaminterface">FindUpstreamInterface</a>
</td>
<td align="left" width="63%">
Searches the filter graph for a specified interface, upstream from a specified pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamgraphstreams-setmaxgraphlatency">SetMaxGraphLatency</a>
</td>
<td align="left" width="63%">
Sets the maximum latency for the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset">SyncUsingStreamOffset</a>
</td>
<td align="left" width="63%">
Enables or disables synchronization using time-stamp offsets.

</td>
</tr>
</table> 

