---
UID: NF:evr.IMFVideoMixerControl.SetStreamZOrder
title: IMFVideoMixerControl::SetStreamZOrder (evr.h)
description: Sets the z-order of a video stream.
helpviewer_keywords: ["6187724a-6345-4feb-90a0-097b6d21180f","IMFVideoMixerControl interface [Media Foundation]","SetStreamZOrder method","IMFVideoMixerControl.SetStreamZOrder","IMFVideoMixerControl::SetStreamZOrder","SetStreamZOrder","SetStreamZOrder method [Media Foundation]","SetStreamZOrder method [Media Foundation]","IMFVideoMixerControl interface","evr/IMFVideoMixerControl::SetStreamZOrder","mf.imfvideomixercontrol_setstreamzorder"]
old-location: mf\imfvideomixercontrol_setstreamzorder.htm
tech.root: mfarchive
ms.assetid: 6187724a-6345-4feb-90a0-097b6d21180f
ms.date: 12/05/2018
ms.keywords: 6187724a-6345-4feb-90a0-097b6d21180f, IMFVideoMixerControl interface [Media Foundation],SetStreamZOrder method, IMFVideoMixerControl.SetStreamZOrder, IMFVideoMixerControl::SetStreamZOrder, SetStreamZOrder, SetStreamZOrder method [Media Foundation], SetStreamZOrder method [Media Foundation],IMFVideoMixerControl interface, evr/IMFVideoMixerControl::SetStreamZOrder, mf.imfvideomixercontrol_setstreamzorder
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoMixerControl::SetStreamZOrder
 - evr/IMFVideoMixerControl::SetStreamZOrder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoMixerControl.SetStreamZOrder
archived: true
---

# IMFVideoMixerControl::SetStreamZOrder


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets the z-order of a video stream.

## -parameters

### -param dwStreamID [in]

Identifier of the stream. For the EVR media sink, the stream identifier is defined when the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a> method is called. For the DirectShow EVR filter, the stream identifier corresponds to the pin index. The reference stream is always stream 0.

### -param dwZ [in]

Z-order value. The z-order of the reference stream must be zero. The maximum z-order value is the number of streams minus one.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>dwZ</i> is larger than the maximum z-order value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid z-order for this stream. For the reference stream, <i>dwZ</i> must be zero. For all other streams, <i>dwZ</i> must be greater than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream identifier.

</td>
</tr>
</table>

## -remarks

The EVR draws the video streams in the order of their z-order values, starting with zero. The reference stream must be first in the z-order, and the remaining streams can be in any order.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol">IMFVideoMixerControl</a>