---
UID: NN:mfcaptureengine.IMFCaptureSink
title: IMFCaptureSink (mfcaptureengine.h)
description: Controls a capture sink, which is an object that receives one or more streams from a capture device.
helpviewer_keywords: ["IMFCaptureSink","IMFCaptureSink interface [Media Foundation]","IMFCaptureSink interface [Media Foundation]","described","mf.imfcapturesink","mfcaptureengine/IMFCaptureSink"]
old-location: mf\imfcapturesink.htm
tech.root: mf
ms.assetid: FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE
ms.date: 12/05/2018
ms.keywords: IMFCaptureSink, IMFCaptureSink interface [Media Foundation], IMFCaptureSink interface [Media Foundation],described, mf.imfcapturesink, mfcaptureengine/IMFCaptureSink
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
 - IMFCaptureSink
 - mfcaptureengine/IMFCaptureSink
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
 - IMFCaptureSink
---

# IMFCaptureSink interface


## -description

Controls a capture sink, which is an object that receives one or more streams from a capture device.

## -inheritance

The <b>IMFCaptureSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureSink</b> also has these types of members:

## -remarks

The capture engine creates the following capture sinks.

<ul>
<li>Photo sink. Encodes still image files.</li>
<li>Preview sink. Previews live audio or video.</li>
<li>Recording sink. Creates compressed audio/video files or compressed audio/video streams.</li>
</ul>
To get a pointer to a capture sink, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-getsink">IMFCaptureEngine::GetSink</a>. Each capture sink implements an interface that derives from <b>IMFCaptureSink</b>. Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to get a pointer to the derived interface.<table>
<tr>
<th>Sink</th>
<th>Interface</th>
</tr>
<tr>
<td>Photo sink</td>
<td>
<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink">IMFCapturePhotoSink</a>
</td>
</tr>
<tr>
<td>Preview sink</td>
<td>
<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink">IMFCapturePreviewSink</a>
</td>
</tr>
<tr>
<td>Recording sink</td>
<td>
<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink">IMFCaptureRecordSink</a>
</td>
</tr>
</table>
 



Applications cannot directly create the capture sinks.

If an image stream native media type is set to JPEG, the photo sink should be configured with a format identical to native source format. JPEG native type is passthrough only.

If an image stream native type is set to JPEG, to add an effect, change the native type on the image stream to an uncompressed video media type (such as NV12 or RGB32) and then add the effect.

If the native type is H.264 for the record stream, the record sink should be configured with the same media type. H.264 native type is passthrough only and cannot be decoded.

Record streams that expose H.264 do not  expose any other type. H.264 record streams cannot be used in conjunction with effects. To add effects, instead connect the preview stream to the recordsink using <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">AddStream</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
