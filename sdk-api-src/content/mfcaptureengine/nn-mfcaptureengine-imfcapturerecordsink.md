---
UID: NN:mfcaptureengine.IMFCaptureRecordSink
title: IMFCaptureRecordSink (mfcaptureengine.h)
author: windows-sdk-content
description: Controls the recording sink.
old-location: mf\imfcapturerecordsink.htm
tech.root: medfound
ms.assetid: AEF5923D-C4ED-4BEA-A969-163ED837A5BD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFCaptureRecordSink, IMFCaptureRecordSink interface [Media Foundation], IMFCaptureRecordSink interface [Media Foundation],described, mf.imfcapturerecordsink, mfcaptureengine/IMFCaptureRecordSink
ms.topic: interface
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
 - IMFCaptureRecordSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCaptureRecordSink interface


## -description


Controls the recording sink. The recording sink creates compressed audio/video files or compressed audio/video streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureRecordSink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>. <b>IMFCaptureRecordSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureRecordSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-getrotation">GetRotation</a>
</td>
<td align="left" width="63%">
Gets the rotation that is currently being applied to the recorded video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setcustomsink">SetCustomSink</a>
</td>
<td align="left" width="63%">
Sets a custom media sink for recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setoutputbytestream">SetOutputByteStream</a>
</td>
<td align="left" width="63%">
Specifies a byte stream that will receive the data for the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setoutputfilename">SetOutputFileName</a>
</td>
<td align="left" width="63%">
Specifies the name of the output file for the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setrotation">SetRotation</a>
</td>
<td align="left" width="63%">
Rotates the recorded video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setsamplecallback">SetSampleCallback</a>
</td>
<td align="left" width="63%">
Sets a callback to receive the recording data for one stream.

</td>
</tr>
</table> 


## -remarks



The recording sink can deliver samples to one of the following destinations:

<ul>
<li>Byte stream.</li>
<li>Output file.</li>
<li>Application-provided callback interface.</li>
</ul>
The application must specify a single destination. Multiple destinations are not supported. (However, if a callback is used, you can provide a separate callback for each stream.)

If the destination is a byte stream or an output file, the application specifies a container type, such as MP4 or ASF. The capture engine then multiplexes the audio and video to produce the format defined by the container type. If the destination is a callback interface, however, the capture engine does not multiplex or otherwise interleave the samples. The callback option gives you the most control over the recorded output, but requires more work by the application.

To start the recording, call <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-startrecord">IMFCaptureEngine::StartRecord</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

