---
UID: NN:segment.IMSVidGenericSink
title: IMSVidGenericSink (segment.h)
author: windows-sdk-content
description: The IMSVidGenericSink interface represents a generic output device that supports streaming output. It is implemented by the MSVidGenericSink object.
old-location: mstv\imsvidgenericsink.htm
tech.root: mstv
ms.assetid: 15181a89-aa64-4ecf-aaf5-4aac36753ddf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidGenericSink, IMSVidGenericSink interface [Microsoft TV Technologies], IMSVidGenericSink interface [Microsoft TV Technologies],described, IMSVidGenericSinkInterface, mstv.imsvidgenericsink, segment/IMSVidGenericSink
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidGenericSink"
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMSVidGenericSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidGenericSink interface


## -description



<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
        </div>
<div> </div>


The <b>IMSVidGenericSink</b> interface represents a generic output device that supports streaming output. It is implemented by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695128(v=vs.85)">MSVidGenericSink</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidGenericSink</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>. <b>IMSVidGenericSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidGenericSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidgenericsink-get_sinkstreams">get_SinkStreams</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidgenericsink-put_sinkstreams">put_SinkStreams</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidgenericsink-setsinkfilter">SetSinkFilter</a>
</td>
<td align="left" width="63%">
Sets the filter for the sink.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidGenericSink)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

