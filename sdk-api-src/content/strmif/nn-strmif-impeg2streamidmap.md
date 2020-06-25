---
UID: NN:strmif.IMPEG2StreamIdMap
title: IMPEG2StreamIdMap (strmif.h)
description: This interface is implemented on each output pin of the MPEG-2 Demultiplexer filter (Demux) and is used in program stream mode only.
helpviewer_keywords: ["IMPEG2StreamIdMap","IMPEG2StreamIdMap interface [DirectShow]","IMPEG2StreamIdMap interface [DirectShow]","described","IMPEG2StreamIdMapInterface","dshow.impeg2streamidmap","strmif/IMPEG2StreamIdMap"]
old-location: dshow\impeg2streamidmap.htm
tech.root: DirectShow
ms.assetid: 714c6b0e-3885-4026-8a83-06b37cc97d7c
ms.date: 12/05/2018
ms.keywords: IMPEG2StreamIdMap, IMPEG2StreamIdMap interface [DirectShow], IMPEG2StreamIdMap interface [DirectShow],described, IMPEG2StreamIdMapInterface, dshow.impeg2streamidmap, strmif/IMPEG2StreamIdMap
f1_keywords:
- strmif/IMPEG2StreamIdMap
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
- IMPEG2StreamIdMap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMPEG2StreamIdMap interface


## -description



This interface is implemented on each output pin of the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/mpeg-2-demultiplexer">MPEG-2 Demultiplexer</a> filter (Demux) and is used in program stream mode only. It is called by applications or other filters to associate the pin with a specified Stream ID and to inform the pin whether substream filtering is required on the stream. This interface is not exposed when the filter is playing back a file (pull-mode).

For transport streams, use the <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-impeg2pidmap">IMPEG2PIDMap</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2StreamIdMap</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMPEG2StreamIdMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2StreamIdMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-impeg2streamidmap-enumstreamidmap">EnumStreamIdMap</a>
</td>
<td align="left" width="63%">
Returns a collection of all the mapped Stream IDs on this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-impeg2streamidmap-mapstreamid">MapStreamId</a>
</td>
<td align="left" width="63%">
Maps the Stream ID of an elementary stream within an MPEG-2 program stream to a media content type and substream filtering information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-impeg2streamidmap-unmapstreamid">UnmapStreamId</a>
</td>
<td align="left" width="63%">
Unmaps the Stream ID mapping created in a previous call to <b>MapStreamId</b>.

</td>
</tr>
</table> 

