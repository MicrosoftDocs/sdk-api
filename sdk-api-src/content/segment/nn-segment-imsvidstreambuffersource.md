---
UID: NN:segment.IMSVidStreamBufferSource
title: IMSVidStreamBufferSource (segment.h)
description: The IMSVidStreamBufferSource interface represents the Stream Buffer Source filter within the Video Control.
old-location: mstv\imsvidstreambuffersource.htm
tech.root: mstv
ms.assetid: 12160959-820b-4534-9392-a13ad229317d
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource, IMSVidStreamBufferSource interface [Microsoft TV Technologies], IMSVidStreamBufferSource interface [Microsoft TV Technologies],described, IMSVidStreamBufferSourceInterface, mstv.imsvidstreambuffersource, segment/IMSVidStreamBufferSource
f1_keywords:
- segment/IMSVidStreamBufferSource
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
- IMSVidStreamBufferSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSource interface


## -description



The <b>IMSVidStreamBufferSource</b> interface represents the Stream Buffer Source filter within the Video Control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSource</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidfileplayback">IMSVidFilePlayback</a>. <b>IMSVidStreamBufferSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource-currentratings">CurrentRatings</a>
</td>
<td align="left" width="63%">
Retrieves the current ratings information from the data source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource-get_recordingattribute">get_RecordingAttribute</a>
</td>
<td align="left" width="63%">
Retrieves the Stream Buffer Source filter that this object manages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource-get_sbesource">get_SBESource</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the Stream Buffer Source filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource-get_start">get_Start</a>
</td>
<td align="left" width="63%">
Retrieves the start time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource-maxratingslevel">MaxRatingsLevel</a>
</td>
<td align="left" width="63%">
Specifies the maximum ratings level the object is permitted to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource-put_blockunrated">put_BlockUnrated</a>
</td>
<td align="left" width="63%">
Specifies whether to block unrated content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource-put_unrateddelay">put_UnratedDelay</a>
</td>
<td align="left" width="63%">
Specifies the amount of time to play unrated content before blocking it.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSource)</code>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidfileplayback">IMSVidFilePlayback</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

