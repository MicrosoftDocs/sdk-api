---
UID: NN:mfcaptureengine.IMFCaptureRecordSink
title: IMFCaptureRecordSink
author: windows-sdk-content
description: Controls the recording sink.
old-location: mf\imfcapturerecordsink.htm
tech.root: medfound
ms.assetid: AEF5923D-C4ED-4BEA-A969-163ED837A5BD
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IMFCaptureRecordSink, IMFCaptureRecordSink interface [Media Foundation], IMFCaptureRecordSink interface [Media Foundation],described, mf.imfcapturerecordsink, mfcaptureengine/IMFCaptureRecordSink
ms.prod: windows
ms.technology: windows-sdk
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
---

# IMFCaptureRecordSink interface


## -description


Controls the recording sink. The recording sink creates compressed audio/video files or compressed audio/video streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureRecordSink</b> interface inherits from <a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>. <b>IMFCaptureRecordSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E582ED9C-D7B8-4DF9-B72F-361E682DB93F">GetRotation</a>
</td>
<td align="left" width="63%">
Gets the rotation that is currently being applied to the recorded video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76140ECF-E7A2-4C41-A710-813B2DF8F52C">SetCustomSink</a>
</td>
<td align="left" width="63%">
Sets a custom media sink for recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C33357C8-882A-4350-8638-46C2220FC445">SetOutputByteStream</a>
</td>
<td align="left" width="63%">
Specifies a byte stream that will receive the data for the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96BEE09C-1B17-4857-B0DC-553D14B908E7">SetOutputFileName</a>
</td>
<td align="left" width="63%">
Specifies the name of the output file for the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3C451FF9-F5CD-48C6-A7FE-88BD3E82DA83">SetRotation</a>
</td>
<td align="left" width="63%">
Rotates the recorded video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1D7BB0D1-3F77-4AF3-9624-73EE4D0D0BCE">SetSampleCallback</a>
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

To start the recording, call <a href="https://msdn.microsoft.com/22084409-B2E6-47EF-A59B-A762E9A9191D">IMFCaptureEngine::StartRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

