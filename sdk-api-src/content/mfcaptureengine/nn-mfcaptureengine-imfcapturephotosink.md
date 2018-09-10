---
UID: NN:mfcaptureengine.IMFCapturePhotoSink
title: IMFCapturePhotoSink
author: windows-sdk-content
description: Controls the photo sink.
old-location: mf\imfcapturephotosink.htm
tech.root: medfound
ms.assetid: 14BB9A86-47F2-4CFE-A932-3F2C7B6AF2BA
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFCapturePhotoSink, IMFCapturePhotoSink interface [Media Foundation], IMFCapturePhotoSink interface [Media Foundation],described, mf.imfcapturephotosink, mfcaptureengine/IMFCapturePhotoSink
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
 - IMFCapturePhotoSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCapturePhotoSink interface


## -description


Controls the photo sink. The photo sink captures still images from the video stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCapturePhotoSink</b> interface inherits from <a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>. <b>IMFCapturePhotoSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/D67C2D66-FC40-4AF3-9E83-29D0DBF99AD3">SetOutputByteStream</a>
</td>
<td align="left" width="63%">
Specifies a byte stream that will receive the still image data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CAA9F7CF-A92F-4039-BEA5-07A730E82EE4">SetOutputFileName</a>
</td>
<td align="left" width="63%">
Specifies the name of the output file for the still image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/595716F6-8059-4B56-9FB3-906846BA3CBB">SetSampleCallback</a>
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

To capture an image, call <a href="https://msdn.microsoft.com/6E633E90-9C8B-44B6-9149-704872143147">IMFCaptureEngine::TakePhoto</a>.




## -see-also




<a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

