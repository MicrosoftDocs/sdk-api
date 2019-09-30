---
UID: NN:segment.IMSVidClosedCaptioning
title: IMSVidClosedCaptioning (segment.h)
author: windows-sdk-content
description: The IMSVidClosedCaptioning interface enables or disables closed captions.
old-location: mstv\imsvidclosedcaptioning.htm
tech.root: mstv
ms.assetid: 070a208b-cf4c-41e1-9a5f-76cc444285c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidClosedCaptioning, IMSVidClosedCaptioning interface [Microsoft TV Technologies], IMSVidClosedCaptioning interface [Microsoft TV Technologies],described, IMSVidClosedCaptioningInterface, mstv.imsvidclosedcaptioning, segment/IMSVidClosedCaptioning
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidClosedCaptioning"
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
 - IMSVidClosedCaptioning
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidClosedCaptioning interface


## -description



The <b>IMSVidClosedCaptioning</b> interface enables or disables closed captions. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695119(v=vs.85)">MSVidClosedCaptioning</a> feature exposes this interface.

To obtain this interface, enumerate the collection of available features on the Video Control. To use closed captioning, activate the closed captioning feature before you build the graph. Once the feature is active, you can enable or disable the closed captioning display by calling the <a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidclosedcaptioning-put_enable">IMSVidClosedCaptioning::put_Enable</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidClosedCaptioning</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidfeature">IMSVidFeature</a>. <b>IMSVidClosedCaptioning</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidClosedCaptioning</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidclosedcaptioning-get_enable">get_Enable</a>
</td>
<td align="left" width="63%">
Queries whether closed captioning is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidclosedcaptioning-put_enable">put_Enable</a>
</td>
<td align="left" width="63%">
Enables or disables closed captioning.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidClosedCaptioning)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/displaying-closed-captioning-in-c">Displaying Closed Captioning in C++</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidfeature">IMSVidFeature</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

