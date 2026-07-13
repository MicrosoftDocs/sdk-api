---
UID: NF:evr.IMFVideoRenderer.InitializeRenderer
title: IMFVideoRenderer::InitializeRenderer (evr.h)
description: Sets a new mixer or presenter for the enhanced video renderer (EVR).
helpviewer_keywords: ["IMFVideoRenderer interface [Media Foundation]","InitializeRenderer method","IMFVideoRenderer.InitializeRenderer","IMFVideoRenderer::InitializeRenderer","InitializeRenderer","InitializeRenderer method [Media Foundation]","InitializeRenderer method [Media Foundation]","IMFVideoRenderer interface","e46a9596-9f3f-4430-8d45-bbc9c240be3b","evr/IMFVideoRenderer::InitializeRenderer","mf.imfvideorenderer_initializerenderer"]
old-location: mf\imfvideorenderer_initializerenderer.htm
tech.root: mfarchive
ms.assetid: e46a9596-9f3f-4430-8d45-bbc9c240be3b
ms.date: 12/05/2018
ms.keywords: IMFVideoRenderer interface [Media Foundation],InitializeRenderer method, IMFVideoRenderer.InitializeRenderer, IMFVideoRenderer::InitializeRenderer, InitializeRenderer, InitializeRenderer method [Media Foundation], InitializeRenderer method [Media Foundation],IMFVideoRenderer interface, e46a9596-9f3f-4430-8d45-bbc9c240be3b, evr/IMFVideoRenderer::InitializeRenderer, mf.imfvideorenderer_initializerenderer
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
 - IMFVideoRenderer::InitializeRenderer
 - evr/IMFVideoRenderer::InitializeRenderer
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
 - IMFVideoRenderer.InitializeRenderer
archived: true
---

# IMFVideoRenderer::InitializeRenderer


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets a new mixer or presenter for the enhanced video renderer (EVR).

## -parameters

### -param pVideoMixer [in]

Pointer to the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface of the mixer to use. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the EVR uses its default mixer.

### -param pVideoPresenter [in]

Pointer to the <a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter">IMFVideoPresenter</a> interface of the presenter to use. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the EVR uses its default presenter.

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
Either the mixer or the presenter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The mixer and presenter cannot be replaced in the current state. (EVR media sink.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
One or more input pins are connected. (DirectShow EVR filter.)

</td>
</tr>
</table>

## -remarks

Call this method directly after creating the EVR, before you do any of the following:

<ul>
<li>
Call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the EVR.

</li>
<li>
Call <a href="/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams">IEVRFilterConfig::SetNumberOfStreams</a> on the EVR.

</li>
<li>
Connect any pins on the EVR filter, or set any media types on EVR media sink.

</li>
</ul>
The EVR filter returns VFW_E_WRONG_STATE if any of the filter's pins are connected. The EVR media sink returns MF_E_INVALIDREQUEST if a media type is set on any of the streams, or the presentation clock is running or paused.

The device identifiers for the mixer and the presenter must match. The <a href="/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid">IMFVideoDeviceID::GetDeviceID</a> method returns the device identifier. If they do not match, the method returns E_INVALIDARG.

If the video renderer is in the protected media path (PMP), the mixer and presenter objects must be certified safe components and pass any trust authority verification that is being enforced. Otherwise, this method will fail.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer">IMFVideoRenderer</a>