---
UID: NN:segment.IMSVidTunerEvent
title: IMSVidTunerEvent (segment.h)

description: This topic applies to Windows XP or later.
old-location: mstv\imsvidtunerevent.htm
tech.root: mstv
ms.assetid: cdffe6ca-00b0-4230-963d-b4409413e5f5

ms.date: 12/05/2018
ms.keywords: IMSVidTunerEvent, IMSVidTunerEvent interface [Microsoft TV Technologies], IMSVidTunerEvent interface [Microsoft TV Technologies],described, IMSVidTunerEventInterface, mstv.imsvidtunerevent, segment/IMSVidTunerEvent
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidTunerEvent"
dev_langs:
 - c++
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
 - IMSVidTunerEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidTunerEvent interface


## -description



This topic applies to Windows XP or later.
        

The <b>IMSVidTunerEvent</b> interface is used to receive events from BDA-compliant digital TV tuners.

This interface is an outgoing connection-point interface. To receive events from a BDA digital tuner, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidbdatunerdevice">MSVidBDATunerDevice</a> object to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidTunerEvent</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/segment/nn-segment-imsvidinputdeviceevent">IMSVidInputDeviceEvent</a>. <b>IMSVidTunerEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidTunerEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidtunerevent-tunechanged">TuneChanged</a>
</td>
<td align="left" width="63%">
Signals that the tuner has tuned to a new frequency.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidTunerEvent)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/segment/nn-segment-imsvidinputdeviceevent">IMSVidInputDeviceEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
 

 

