---
UID: NN:mfcaptureengine.IMFCaptureRecordSink
title: IMFCaptureRecordSink (mfcaptureengine.h)
description: Controls the recording sink.
helpviewer_keywords: ["IMFCaptureRecordSink","IMFCaptureRecordSink interface [Media Foundation]","IMFCaptureRecordSink interface [Media Foundation]","described","mf.imfcapturerecordsink","mfcaptureengine/IMFCaptureRecordSink"]
old-location: mf\imfcapturerecordsink.htm
tech.root: mf
ms.assetid: AEF5923D-C4ED-4BEA-A969-163ED837A5BD
ms.date: 12/05/2018
ms.keywords: IMFCaptureRecordSink, IMFCaptureRecordSink interface [Media Foundation], IMFCaptureRecordSink interface [Media Foundation],described, mf.imfcapturerecordsink, mfcaptureengine/IMFCaptureRecordSink
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
 - IMFCaptureRecordSink
 - mfcaptureengine/IMFCaptureRecordSink
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
 - IMFCaptureRecordSink
---

# IMFCaptureRecordSink interface


## -description

Controls the recording sink. The recording sink creates compressed audio/video files or compressed audio/video streams.

## -inheritance

The <b>IMFCaptureRecordSink</b> interface inherits from <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>. <b>IMFCaptureRecordSink</b> also has these types of members:

## -remarks

The recording sink can deliver samples to one of the following destinations:

<ul>
<li>Byte stream.</li>
<li>Output file.</li>
<li>Application-provided callback interface.</li>
</ul>
The application must specify a single destination. Multiple destinations are not supported. (However, if a callback is used, you can provide a separate callback for each stream.)

If the destination is a byte stream or an output file, the application specifies a container type, such as MP4 or ASF. The capture engine then multiplexes the audio and video to produce the format defined by the container type. If the destination is a callback interface, however, the capture engine does not multiplex or otherwise interleave the samples. The callback option gives you the most control over the recorded output, but requires more work by the application.

To start the recording, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-startrecord">IMFCaptureEngine::StartRecord</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
