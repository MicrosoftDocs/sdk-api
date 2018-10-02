---
UID: NN:mfcaptureengine.IMFCaptureSource
title: IMFCaptureSource
author: windows-sdk-content
description: Controls the capture source object. The capture source manages the audio and video capture devices.
old-location: mf\imfcapturesource.htm
tech.root: MedFound
ms.assetid: 864B6B5D-EB7E-4C49-A326-9B6704A27635
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IMFCaptureSource, IMFCaptureSource interface [Media Foundation], IMFCaptureSource interface [Media Foundation],described, mf.imfcapturesource, mfcaptureengine/IMFCaptureSource
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
 - IMFCaptureSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSource interface


## -description


Controls the capture source object. The capture source manages the audio and video capture devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFCaptureSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C108360D-0B8C-4539-9D78-A5559100086E">AddEffect</a>
</td>
<td align="left" width="63%">
Adds an effect to a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B122C2DE-9544-47C7-8F4F-DBD4C1DE54C0">GetAvailableDeviceMediaType</a>
</td>
<td align="left" width="63%">
Gets a format that is supported by one of the capture streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f69321f-67df-4d6c-a98a-51a9859f8a22">GetCaptureDeviceActivate</a>
</td>
<td align="left" width="63%">
 Gets the current capture device's <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> object pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98bce6e3-02f2-449e-aba4-4bfc9de6d1db">GetCaptureDeviceSource</a>
</td>
<td align="left" width="63%">
Gets the current capture device's <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> object pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8F263F5C-D1B4-4DF7-AFCB-E27575FBAAA2">GetCurrentDeviceMediaType</a>
</td>
<td align="left" width="63%">
Gets the current media type for a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3caa002-8676-44d3-9696-da5b0db09d9e">GetDeviceStreamCategory</a>
</td>
<td align="left" width="63%">
Gets the stream category for the specified source stream index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0CD466EF-4753-42F6-A9B9-71CBB0668342">GetDeviceStreamCount</a>
</td>
<td align="left" width="63%">
Gets the number of device streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3FB15EC5-DE9C-4051-9FBA-7CE332E70078">GetMirrorState</a>
</td>
<td align="left" width="63%">
Gets the current mirroring state of the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67A77196-A499-4C28-8A35-CFB130B85D79">GetService</a>
</td>
<td align="left" width="63%">
Gets a pointer to the underlying <a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38bc2ca8-29ff-4a23-9b78-693aaab6767f">GetStreamIndexFromFriendlyName</a>
</td>
<td align="left" width="63%">
Gets the actual device stream index translated from a friendly stream name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C01F7A61-3585-4E8B-B914-7DB1446D1BC1">RemoveAllEffects</a>
</td>
<td align="left" width="63%">
Removes all effects from a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5FF2EF1C-1BF0-4CF7-95AB-1BB10025D66F">RemoveEffect</a>
</td>
<td align="left" width="63%">
Removes an effect from a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2B88BBAE-E837-4F4A-B697-64772F25C89D">SetCurrentDeviceMediaType</a>
</td>
<td align="left" width="63%">
Sets the output format for a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E170B262-95CD-4434-925A-3573D35FC1DC">SetMirrorState</a>
</td>
<td align="left" width="63%">
Enables or disables mirroring of the video preview stream.

</td>
</tr>
</table> 


## -remarks



To get a pointer to the capture source, call <a href="https://msdn.microsoft.com/9DED11CA-BDBB-4E1A-BAD1-2EB6216543F9">IMFCaptureEngine::GetSource</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

