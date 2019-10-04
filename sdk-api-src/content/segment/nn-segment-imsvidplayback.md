---
UID: NN:segment.IMSVidPlayback
title: IMSVidPlayback (segment.h)
author: windows-sdk-content
description: The IMSVidPlayback interface controls a Video Control playback device.
old-location: mstv\imsvidplayback.htm
tech.root: mstv
ms.assetid: ed954545-f58f-4841-9ffd-185350f76388
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback, IMSVidPlayback interface [Microsoft TV Technologies], IMSVidPlayback interface [Microsoft TV Technologies],described, IMSVidPlaybackInterface, mstv.imsvidplayback, segment/IMSVidPlayback
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidPlayback"
dev_langs:
 - c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IMSVidPlayback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidPlayback interface


## -description



The <b>IMSVidPlayback</b> interface controls a Video Control playback device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidPlayback</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidinputdevice">IMSVidInputDevice</a>. <b>IMSVidPlayback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidPlayback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-get_canstep">get_CanStep</a>
</td>
<td align="left" width="63%">
Queries whether the input source can step frame by frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-get_currentposition">get_CurrentPosition</a>
</td>
<td align="left" width="63%">
Returns the current playback position of the source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-get_enableresetonstop">get_EnableResetOnStop</a>
</td>
<td align="left" width="63%">
Indicates how playback will resume if the graph is rebuilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-get_length">get_Length</a>
</td>
<td align="left" width="63%">
Retrieves the length of the playback source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-get_positionmode">get_PositionMode</a>
</td>
<td align="left" width="63%">
Indicates how position values are interpreted by this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-get_rate">get_Rate</a>
</td>
<td align="left" width="63%">
Retrieves the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the playback device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-put_currentposition">put_CurrentPosition</a>
</td>
<td align="left" width="63%">
Seeks to a specified position in the source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-put_enableresetonstop">put_EnableResetOnStop</a>
</td>
<td align="left" width="63%">
Specifies how playback will resume if the graph is rebuilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-put_positionmode">put_PositionMode</a>
</td>
<td align="left" width="63%">
Specifies how position values will be interpreted by this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-put_rate">put_Rate</a>
</td>
<td align="left" width="63%">
Sets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-run">Run</a>
</td>
<td align="left" width="63%">
Runs the playback device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-step">Step</a>
</td>
<td align="left" width="63%">
Steps through the video stream by a specified number of frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidplayback-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the playback device.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidPlayback)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidinputdevice">IMSVidInputDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

