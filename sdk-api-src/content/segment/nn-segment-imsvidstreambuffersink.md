---
UID: NN:segment.IMSVidStreamBufferSink
title: IMSVidStreamBufferSink (segment.h)
description: The IMSVidStreamBufferSink interface represents the Stream Buffer Sink filter within the Video Control.
helpviewer_keywords: ["IMSVidStreamBufferSink","IMSVidStreamBufferSink interface [Microsoft TV Technologies]","IMSVidStreamBufferSink interface [Microsoft TV Technologies]","described","IMSVidStreamBufferSinkInterface","mstv.imsvidstreambuffersink","segment/IMSVidStreamBufferSink"]
old-location: mstv\imsvidstreambuffersink.htm
tech.root: mstv
ms.assetid: 80f6cd3a-8cb8-4bda-9b66-33e7d214015a
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink, IMSVidStreamBufferSink interface [Microsoft TV Technologies], IMSVidStreamBufferSink interface [Microsoft TV Technologies],described, IMSVidStreamBufferSinkInterface, mstv.imsvidstreambuffersink, segment/IMSVidStreamBufferSink
f1_keywords:
- segment/IMSVidStreamBufferSink
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
- segment.h
api_name:
- IMSVidStreamBufferSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSink interface


## -description



The <b>IMSVidStreamBufferSink</b> interface represents the Stream Buffer Sink filter within the Video Control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSink</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>. <b>IMSVidStreamBufferSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-get_contentrecorder">get_ContentRecorder</a>
</td>
<td align="left" width="63%">
Creates a new content recording object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-get_referencerecorder">get_ReferenceRecorder</a>
</td>
<td align="left" width="63%">
Creates a new reference recording object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-get_sbesink">get_SBESink</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the Stream Buffer Sink filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-get_sinkname">get_SinkName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the stub file that points to the backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-namesetlock">NameSetLock</a>
</td>
<td align="left" width="63%">
Locks the stream buffer profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-put_sinkname">put_SinkName</a>
</td>
<td align="left" width="63%">
Sets the name of the stub file that points to the backing files.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSink)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

