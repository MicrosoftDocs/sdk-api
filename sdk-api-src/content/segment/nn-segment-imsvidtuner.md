---
UID: NN:segment.IMSVidTuner
title: IMSVidTuner (segment.h)
author: windows-sdk-content
description: The IMSVidTuner interface manages tuning devices.
old-location: mstv\imsvidtuner.htm
tech.root: mstv
ms.assetid: b11f3ac4-c351-4017-9801-98d8edec7449
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidTuner, IMSVidTuner interface [Microsoft TV Technologies], IMSVidTuner interface [Microsoft TV Technologies],described, IMSVidTunerInterface, mstv.imsvidtuner, segment/IMSVidTuner
ms.topic: interface
f1_keywords: ["segment/IMSVidTuner"]
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
 - IMSVidTuner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidTuner interface


## -description



The <b>IMSVidTuner</b> interface manages tuning devices. It is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidbdatunerdevice">MSVidBDATunerDevice</a> object, which represents Broadcast Driver Architecture (BDA)-compliant tuning devices. Non-BDA analog tuners expose the <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner</a> interface, which inherits from this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidTuner</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideoinputdevice">IMSVidVideoInputDevice</a>. <b>IMSVidTuner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidTuner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidtuner-get_tune">get_Tune</a>
</td>
<td align="left" width="63%">
Retrieves the current tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidtuner-get_tuningspace">get_TuningSpace</a>
</td>
<td align="left" width="63%">
Retrieves the current tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidtuner-put_tune">put_Tune</a>
</td>
<td align="left" width="63%">
Specifies the tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidtuner-put_tuningspace">put_TuningSpace</a>
</td>
<td align="left" width="63%">
Specifies the tuning space.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidTuner)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideoinputdevice">IMSVidVideoInputDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

