---
UID: NN:mfcaptureengine.IMFCapturePhotoSink
title: IMFCapturePhotoSink (mfcaptureengine.h)
author: windows-sdk-content
description: Controls the photo sink.
old-location: mf\imfcapturephotosink.htm
tech.root: medfound
ms.assetid: 14BB9A86-47F2-4CFE-A932-3F2C7B6AF2BA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFCapturePhotoSink, IMFCapturePhotoSink interface [Media Foundation], IMFCapturePhotoSink interface [Media Foundation],described, mf.imfcapturephotosink, mfcaptureengine/IMFCapturePhotoSink
ms.topic: interface
f1_keywords: 
 - "mfcaptureengine/IMFCapturePhotoSink"
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
 - IMFCapturePhotoSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCapturePhotoSink interface


## -description


Controls the photo sink. The photo sink captures still images from the video stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCapturePhotoSink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>. <b>IMFCapturePhotoSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCapturePhotoSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturephotosink-setoutputbytestream">SetOutputByteStream</a>
</td>
<td align="left" width="63%">
Specifies a byte stream that will receive the still image data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturephotosink-setoutputfilename">SetOutputFileName</a>
</td>
<td align="left" width="63%">
Specifies the name of the output file for the still image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturephotosink-setsamplecallback">SetSampleCallback</a>
</td>
<td align="left" width="63%">
Sets a callback to receive the still-image data.

</td>
</tr>
</table> 


## -remarks



The photo sink can deliver samples to one of the following destinations:

<ul>
<li>Byte stream.</li>
<li>Output file.</li>
<li>Application-provided callback interface.</li>
</ul>
The application must specify a single destination. Multiple destinations are not supported.

To capture an image, call <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-takephoto">IMFCaptureEngine::TakePhoto</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

