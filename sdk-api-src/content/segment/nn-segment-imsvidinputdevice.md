---
UID: NN:segment.IMSVidInputDevice
title: IMSVidInputDevice (segment.h)
description: The IMSVidInputDevice interface represents any input device that is recognized by the Video Control, such as a television tuner card.
helpviewer_keywords: ["IMSVidInputDevice","IMSVidInputDevice interface [Microsoft TV Technologies]","IMSVidInputDevice interface [Microsoft TV Technologies]","described","IMSVidInputDeviceInterface","mstv.imsvidinputdevice","segment/IMSVidInputDevice"]
old-location: mstv\imsvidinputdevice.htm
tech.root: mstv
ms.assetid: 5b413ade-4ab2-45fa-98b2-fd93c8f89a43
ms.date: 12/05/2018
ms.keywords: IMSVidInputDevice, IMSVidInputDevice interface [Microsoft TV Technologies], IMSVidInputDevice interface [Microsoft TV Technologies],described, IMSVidInputDeviceInterface, mstv.imsvidinputdevice, segment/IMSVidInputDevice
f1_keywords:
- segment/IMSVidInputDevice
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
- IMSVidInputDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidInputDevice interface


## -description



The <b>IMSVidInputDevice</b> interface represents any input device that is recognized by the Video Control, such as a television tuner card. This is a generic interface that serves as an abstract base class for input devices. Several interfaces inherit <b>IMSVidInputDevice</b>, including the following:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidtuner">IMSVidTuner</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner</a>
</li>
</ul>
When a method returns an <b>IMSVidInputDevice</b> pointer, the object that is returned typically supports one of the derived interfaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidInputDevice</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice</a>. <b>IMSVidInputDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidInputDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidinputdevice-isviewable">IsViewable</a>
</td>
<td align="left" width="63%">
Determines whether this device can view the specified tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidinputdevice-view">View</a>
</td>
<td align="left" width="63%">
Configures the input device to view the specified tune request.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidInputDevice)</code>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

