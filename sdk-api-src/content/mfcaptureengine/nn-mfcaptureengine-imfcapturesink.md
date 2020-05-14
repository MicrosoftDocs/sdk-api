---
UID: NN:mfcaptureengine.IMFCaptureSink
title: IMFCaptureSink (mfcaptureengine.h)
description: Controls a capture sink, which is an object that receives one or more streams from a capture device.helpviewer_keywords: ["IMFCaptureSink","IMFCaptureSink interface [Media Foundation]","IMFCaptureSink interface [Media Foundation]","described","mf.imfcapturesink","mfcaptureengine/IMFCaptureSink"]
old-location: mf\imfcapturesink.htm
tech.root: medfound
ms.assetid: FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE
ms.date: 12/05/2018
ms.keywords: IMFCaptureSink, IMFCaptureSink interface [Media Foundation], IMFCaptureSink interface [Media Foundation],described, mf.imfcapturesink, mfcaptureengine/IMFCaptureSink
f1_keywords:
- mfcaptureengine/IMFCaptureSink
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfcaptureengine.h
api_name:
- IMFCaptureSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCaptureSink interface


## -description


Controls a capture sink, which is an object that receives one or more streams from a capture device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">AddStream</a>
</td>
<td align="left" width="63%">
Connects a stream from the capture source to this capture sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-getoutputmediatype">GetOutputMediaType</a>
</td>
<td align="left" width="63%">
Gets the output format for a stream on this capture sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-getservice">GetService</a>
</td>
<td align="left" width="63%">
Queries the underlying <a href="https://docs.microsoft.com/windows/desktop/medfound/sink-writer">Sink Writer</a> object for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-prepare">Prepare</a>
</td>
<td align="left" width="63%">
Prepares the capture sink by loading any required pipeline components, such as encoders, video processors, and media sinks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-removeallstreams">RemoveAllStreams</a>
</td>
<td align="left" width="63%">
Removes all streams from the capture sink.

</td>
</tr>
</table> 


## -remarks



The capture engine creates the following capture sinks.

<ul>
<li>Photo sink. Encodes still image files.</li>
<li>Preview sink. Previews live audio or video.</li>
<li>Recording sink. Creates compressed audio/video files or compressed audio/video streams.</li>
</ul>
To get a pointer to a capture sink, call <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-getsink">IMFCaptureEngine::GetSink</a>. Each capture sink implements an interface that derives from <b>IMFCaptureSink</b>. Call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to get a pointer to the derived interface.<table>
<tr>
<th>Sink</th>
<th>Interface</th>
</tr>
<tr>
<td>Photo sink</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink">IMFCapturePhotoSink</a>
</td>
</tr>
<tr>
<td>Preview sink</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink">IMFCapturePreviewSink</a>
</td>
</tr>
<tr>
<td>Recording sink</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink">IMFCaptureRecordSink</a>
</td>
</tr>
</table>
 



Applications cannot directly create the capture sinks.

If an image stream native media type is set to JPEG, the photo sink should be configured with a format identical to native source format. JPEG native type is passthrough only.

If an image stream native type is set to JPEG, to add an effect, change the native type on the image stream to an uncompressed video media type (such as NV12 or RGB32) and then add the effect.

If the native type is H.264 for the record stream, the record sink should be configured with the same media type. H.264 native type is passthrough only and cannot be decoded.

Record streams that expose H.264 do not  expose any other type. H.264 record streams cannot be used in conjunction with effects. To add effects, instead connect the preview stream to the recordsink using <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">AddStream</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

