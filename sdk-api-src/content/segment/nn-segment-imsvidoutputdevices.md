---
UID: NN:segment.IMSVidOutputDevices
title: IMSVidOutputDevices (segment.h)
description: The IMSVidOutputDevices interface represents a collection of output devices.Output devices include video and audio renderers, and the Stream Buffer Sink object.
helpviewer_keywords: ["IMSVidOutputDevices","IMSVidOutputDevices interface [Microsoft TV Technologies]","IMSVidOutputDevices interface [Microsoft TV Technologies]","described","IMSVidOutputDevicesInterface","mstv.imsvidoutputdevices","segment/IMSVidOutputDevices"]
old-location: mstv\imsvidoutputdevices.htm
tech.root: mstv
ms.assetid: 54776225-ad60-450b-99b4-851cae60ffa7
ms.date: 12/05/2018
ms.keywords: IMSVidOutputDevices, IMSVidOutputDevices interface [Microsoft TV Technologies], IMSVidOutputDevices interface [Microsoft TV Technologies],described, IMSVidOutputDevicesInterface, mstv.imsvidoutputdevices, segment/IMSVidOutputDevices
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidOutputDevices
 - segment/IMSVidOutputDevices
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
 - IMSVidOutputDevices
---

# IMSVidOutputDevices interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidOutputDevices</b> interface represents a collection of output devices.

Output devices include video and audio renderers, and the Stream Buffer Sink object. To obtain the audio and video renders, you can use the following methods:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorendereractive">IMSVidCtl::get_AudioRendererActive</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorenderersavailable">IMSVidCtl::get_AudioRenderersAvailable</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_videorendereractive">IMSVidCtl::get_VideoRendererActive</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_videorenderersavailable">IMSVidCtl::get_VideoRenderersAvailable</a>
</li>
</ul>

## -inheritance

The <b>IMSVidOutputDevices</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidOutputDevices</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidOutputDevices)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
