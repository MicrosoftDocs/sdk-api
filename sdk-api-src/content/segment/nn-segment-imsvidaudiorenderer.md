---
UID: NN:segment.IMSVidAudioRenderer
title: IMSVidAudioRenderer (segment.h)
description: The IMSVidAudioRenderer interface represents an audio renderer device. It enables applications to control the volume and balance. To retrieve the audio renderer device that is currently active, call the IMSVidCtl::get_AudioRendererActive method.
helpviewer_keywords: ["IMSVidAudioRenderer","IMSVidAudioRenderer interface [Microsoft TV Technologies]","IMSVidAudioRenderer interface [Microsoft TV Technologies]","described","IMSVidAudioRendererInterface","mstv.imsvidaudiorenderer","segment/IMSVidAudioRenderer"]
old-location: mstv\imsvidaudiorenderer.htm
tech.root: mstv
ms.assetid: f822b5a6-c88e-48c9-91f4-611a3f147fe0
ms.date: 12/05/2018
ms.keywords: IMSVidAudioRenderer, IMSVidAudioRenderer interface [Microsoft TV Technologies], IMSVidAudioRenderer interface [Microsoft TV Technologies],described, IMSVidAudioRendererInterface, mstv.imsvidaudiorenderer, segment/IMSVidAudioRenderer
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
 - IMSVidAudioRenderer
 - segment/IMSVidAudioRenderer
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
 - IMSVidAudioRenderer
---

# IMSVidAudioRenderer interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidAudioRenderer</b> interface represents an audio renderer device. It enables applications to control the volume and balance. To retrieve the audio renderer device that is currently active, call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorendereractive">IMSVidCtl::get_AudioRendererActive</a> method.

## -inheritance

The <b>IMSVidAudioRenderer</b> interface inherits from <a href="/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>. <b>IMSVidAudioRenderer</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAudioRenderer)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
