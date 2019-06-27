---
UID: NN:strmif.IDVSplitter
title: IDVSplitter (strmif.h)
author: windows-sdk-content
description: Downgrades the frame rate on a digital video (DV) stream.
old-location: dshow\idvsplitter.htm
tech.root: DirectShow
ms.assetid: a7fd27f4-2fc7-4115-b669-b08eed1ec032
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDVSplitter, IDVSplitter interface [DirectShow], IDVSplitter interface [DirectShow],described, IDVSplitterInterface, dshow.idvsplitter, strmif/IDVSplitter
ms.topic: interface
f1_keywords: 
 - "strmif/IDVSplitter"
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
 - IDVSplitter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVSplitter interface


## -description



Downgrades the frame rate on a digital video (DV) stream. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dv-splitter-filter">DV Splitter</a> filter exposes this interface.

Applications can use this interface to reduce the frame rate on a DV stream, before the stream reaches the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dv-video-decoder-filter">DV Video Decoder</a> filter. This can be helpful for processor-intensive tasks, such as real-time transcoding.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVSplitter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVSplitter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVSplitter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvsplitter-discardalternatevideoframes">DiscardAlternateVideoFrames</a>
</td>
<td align="left" width="63%">
Discards half of the frames in the video stream.

</td>
</tr>
</table> 

