---
UID: NN:mfcaptureengine.IMFCaptureSink
title: IMFCaptureSink
author: windows-sdk-content
description: Controls a capture sink, which is an object that receives one or more streams from a capture device.
old-location: mf\imfcapturesink.htm
tech.root: medfound
ms.assetid: FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFCaptureSink, IMFCaptureSink interface [Media Foundation], IMFCaptureSink interface [Media Foundation],described, mf.imfcapturesink, mfcaptureengine/IMFCaptureSink
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
 - IMFCaptureSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSink interface


## -description


Controls a capture sink, which is an object that receives one or more streams from a capture device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFCaptureSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5D7A1FE0-92B9-4CC4-A268-17FA848055A9">AddStream</a>
</td>
<td align="left" width="63%">
Connects a stream from the capture source to this capture sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3F050964-9E71-45FC-9553-A2E7A397217E">GetOutputMediaType</a>
</td>
<td align="left" width="63%">
Gets the output format for a stream on this capture sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/591F0E3D-01A8-420F-86C6-2C610643EB69">GetService</a>
</td>
<td align="left" width="63%">
Queries the underlying <a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a> object for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/244FD291-AD1D-4A51-87C3-C98B33978AA1">Prepare</a>
</td>
<td align="left" width="63%">
Prepares the capture sink by loading any required pipeline components, such as encoders, video processors, and media sinks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7E05D04F-BDE8-4053-A7C4-B74AC5FA76B7">RemoveAllStreams</a>
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
To get a pointer to a capture sink, call <a href="https://msdn.microsoft.com/7DAF5EA3-BA65-4CF9-B7BA-B427A48BF3BC">IMFCaptureEngine::GetSink</a>. Each capture sink implements an interface that derives from <b>IMFCaptureSink</b>. Call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to get a pointer to the derived interface.<table>
<tr>
<th>Sink</th>
<th>Interface</th>
</tr>
<tr>
<td>Photo sink</td>
<td>
<a href="https://msdn.microsoft.com/14BB9A86-47F2-4CFE-A932-3F2C7B6AF2BA">IMFCapturePhotoSink</a>
</td>
</tr>
<tr>
<td>Preview sink</td>
<td>
<a href="https://msdn.microsoft.com/5E64C24D-D6EC-419B-9DC8-309EBCE0077E">IMFCapturePreviewSink</a>
</td>
</tr>
<tr>
<td>Recording sink</td>
<td>
<a href="https://msdn.microsoft.com/AEF5923D-C4ED-4BEA-A969-163ED837A5BD">IMFCaptureRecordSink</a>
</td>
</tr>
</table>
 



Applications cannot directly create the capture sinks.

If an image stream native media type is set to JPEG, the photo sink should be configured with a format identical to native source format. JPEG native type is passthrough only.

If an image stream native type is set to JPEG, to add an effect, change the native type on the image stream to an uncompressed video media type (such as NV12 or RGB32) and then add the effect.

If the native type is H.264 for the record stream, the record sink should be configured with the same media type. H.264 native type is passthrough only and cannot be decoded.

Record streams that expose H.264 do not  expose any other type. H.264 record streams cannot be used in conjunction with effects. To add effects, instead connect the preview stream to the recordsink using <a href="https://msdn.microsoft.com/5D7A1FE0-92B9-4CC4-A268-17FA848055A9">AddStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

