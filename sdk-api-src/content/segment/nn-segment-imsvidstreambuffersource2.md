---
UID: NN:segment.IMSVidStreamBufferSource2
title: IMSVidStreamBufferSource2 (segment.h)
description: The IMSVidStreamBufferSource2 interface represents the Stream Buffer Source filter within the Video Control.
helpviewer_keywords: ["IMSVidStreamBufferSource2","IMSVidStreamBufferSource2 interface [Microsoft TV Technologies]","IMSVidStreamBufferSource2 interface [Microsoft TV Technologies]","described","IMSVidStreamBufferSource2Interface","mstv.imsvidstreambuffersource2","segment/IMSVidStreamBufferSource2"]
old-location: mstv\imsvidstreambuffersource2.htm
tech.root: mstv
ms.assetid: 47012868-4c9e-4974-8549-11331836bed0
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource2, IMSVidStreamBufferSource2 interface [Microsoft TV Technologies], IMSVidStreamBufferSource2 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSource2Interface, mstv.imsvidstreambuffersource2, segment/IMSVidStreamBufferSource2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidStreamBufferSource2
 - segment/IMSVidStreamBufferSource2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSource2
---

# IMSVidStreamBufferSource2 interface


## -description

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div>
<div> </div>


The <b>IMSVidStreamBufferSource2</b> interface represents the Stream Buffer Source filter within the Video Control.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSource2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidstreambuffersource">IMSVidStreamBufferSource</a>. <b>IMSVidStreamBufferSource2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSource2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource2-get_audiocounter">get_AudioCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Source for the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource2-get_cccounter">get_CCCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Source for the closed captioning stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource2-get_videocounter">get_VideoCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Source for the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource2-get_wstcounter">get_WSTCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Source for the World Standard Teletext (WST) stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource2-put_rateex">put_RateEx</a>
</td>
<td align="left" width="63%">
Sets the playback rate, and sets the frame rate for fast-forward play ("trick mode").

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSource2)</code>.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidstreambuffersource">IMSVidStreamBufferSource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>

