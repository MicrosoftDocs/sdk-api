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

The <b>IMSVidAudioRenderer</b> interface represents an audio renderer device. It enables applications to control the volume and balance. To retrieve the audio renderer device that is currently active, call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorendereractive">IMSVidCtl::get_AudioRendererActive</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidAudioRenderer</b> interface inherits from <a href="/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>. <b>IMSVidAudioRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidAudioRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidaudiorenderer-get_balance">get_Balance</a>
</td>
<td align="left" width="63%">
Retrieves the balance level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidaudiorenderer-get_volume">get_Volume</a>
</td>
<td align="left" width="63%">
Retrieves the volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidaudiorenderer-put_balance">put_Balance</a>
</td>
<td align="left" width="63%">
Specifies the balance level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidaudiorenderer-put_volume">put_Volume</a>
</td>
<td align="left" width="63%">
Specifies the volume level.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAudioRenderer)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>