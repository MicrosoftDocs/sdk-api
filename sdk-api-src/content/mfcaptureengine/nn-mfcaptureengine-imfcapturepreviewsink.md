---
UID: NN:mfcaptureengine.IMFCapturePreviewSink
title: IMFCapturePreviewSink (mfcaptureengine.h)
description: Controls the preview sink.
helpviewer_keywords: ["IMFCapturePreviewSink","IMFCapturePreviewSink interface [Media Foundation]","IMFCapturePreviewSink interface [Media Foundation]","described","mf.imfcapturepreviewsink","mfcaptureengine/IMFCapturePreviewSink"]
old-location: mf\imfcapturepreviewsink.htm
tech.root: mf
ms.assetid: 5E64C24D-D6EC-419B-9DC8-309EBCE0077E
ms.date: 12/05/2018
ms.keywords: IMFCapturePreviewSink, IMFCapturePreviewSink interface [Media Foundation], IMFCapturePreviewSink interface [Media Foundation],described, mf.imfcapturepreviewsink, mfcaptureengine/IMFCapturePreviewSink
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFCapturePreviewSink
 - mfcaptureengine/IMFCapturePreviewSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCapturePreviewSink
---

# IMFCapturePreviewSink interface


## -description

Controls the preview sink. The preview sink enables the application to preview audio and video from the camera.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCapturePreviewSink</b> interface inherits from <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>. <b>IMFCapturePreviewSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCapturePreviewSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-getmirrorstate">GetMirrorState</a>
</td>
<td align="left" width="63%">
Gets the current mirroring state of the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-getrotation">GetRotation</a>
</td>
<td align="left" width="63%">
Gets the rotation of the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-setcustomsink">SetCustomSink</a>
</td>
<td align="left" width="63%">
Sets a custom media sink for preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-setmirrorstate">SetMirrorState</a>
</td>
<td align="left" width="63%">
Enables or disables mirroring of the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-setrenderhandle">SetRenderHandle</a>
</td>
<td align="left" width="63%">
Specifies a window for preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-setrendersurface">SetRenderSurface</a>
</td>
<td align="left" width="63%">
Specifies a DirectComposition visual for preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-setrotation">SetRotation</a>
</td>
<td align="left" width="63%">
Rotates the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-setsamplecallback">SetSampleCallback</a>
</td>
<td align="left" width="63%">
Sets a callback to receive the preview data for one stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-updatevideo">UpdateVideo</a>
</td>
<td align="left" width="63%">
Updates the video frame.

</td>
</tr>
</table>

## -remarks

To start preview, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-startpreview">IMFCaptureEngine::StartPreview</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>