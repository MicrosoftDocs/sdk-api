---
UID: NN:segment.IMSVidFilePlayback
title: IMSVidFilePlayback (segment.h)
author: windows-sdk-content
description: The IMSVidFilePlayback interface enables the client to specify a local file for playback. It is implemented by the MSVidFilePlaybackDevice object.
old-location: mstv\imsvidfileplayback.htm
tech.root: mstv
ms.assetid: d6afaf69-5c1b-4f7f-a3cf-51268d6bc2b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidFilePlayback, IMSVidFilePlayback interface [Microsoft TV Technologies], IMSVidFilePlayback interface [Microsoft TV Technologies],described, IMSVidFilePlaybackInterface, mstv.imsvidfileplayback, segment/IMSVidFilePlayback
ms.topic: interface
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
 - IMSVidFilePlayback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidFilePlayback interface


## -description



The <b>IMSVidFilePlayback</b> interface enables the client to specify a local file for playback. It is implemented by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidfileplaybackdevice">MSVidFilePlaybackDevice</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidFilePlayback</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback</a>. <b>IMSVidFilePlayback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidFilePlayback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidfileplayback-get_filename">get_FileName</a>
</td>
<td align="left" width="63%">
Sets the name of the file to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidfileplayback-put_filename">put_FileName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file to play.

</td>
</tr>
</table> 


## -remarks



To play a media file using the Video Control, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">IMSVidCtl::View</a> method with the name of the file. The <b>View</b> method automatically loads the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidfileplaybackdevice">MSVidFilePlayback</a> object.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFilePlayback)</code>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

