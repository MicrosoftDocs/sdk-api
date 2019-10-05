---
UID: NN:mfcaptureengine.IMFCaptureSource
title: IMFCaptureSource (mfcaptureengine.h)
author: windows-sdk-content
description: Controls the capture source object. The capture source manages the audio and video capture devices.
old-location: mf\imfcapturesource.htm
tech.root: medfound
ms.assetid: 864B6B5D-EB7E-4C49-A326-9B6704A27635
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFCaptureSource, IMFCaptureSource interface [Media Foundation], IMFCaptureSource interface [Media Foundation],described, mf.imfcapturesource, mfcaptureengine/IMFCaptureSource
ms.topic: interface
f1_keywords: 
 - "mfcaptureengine/IMFCaptureSource"
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
 - IMFCaptureSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCaptureSource interface


## -description


Controls the capture source object. The capture source manages the audio and video capture devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureSource</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureSource</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-addeffect">AddEffect</a>
</td>
<td align="left" width="63%">
Adds an effect to a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getavailabledevicemediatype">GetAvailableDeviceMediaType</a>
</td>
<td align="left" width="63%">
Gets a format that is supported by one of the capture streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getcapturedeviceactivate">GetCaptureDeviceActivate</a>
</td>
<td align="left" width="63%">
 Gets the current capture device's <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> object pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getcapturedevicesource">GetCaptureDeviceSource</a>
</td>
<td align="left" width="63%">
Gets the current capture device's <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> object pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getcurrentdevicemediatype">GetCurrentDeviceMediaType</a>
</td>
<td align="left" width="63%">
Gets the current media type for a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getdevicestreamcategory">GetDeviceStreamCategory</a>
</td>
<td align="left" width="63%">
Gets the stream category for the specified source stream index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getdevicestreamcount">GetDeviceStreamCount</a>
</td>
<td align="left" width="63%">
Gets the number of device streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getmirrorstate">GetMirrorState</a>
</td>
<td align="left" width="63%">
Gets the current mirroring state of the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getservice">GetService</a>
</td>
<td align="left" width="63%">
Gets a pointer to the underlying <a href="https://docs.microsoft.com/windows/desktop/medfound/source-reader">Source Reader</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getstreamindexfromfriendlyname">GetStreamIndexFromFriendlyName</a>
</td>
<td align="left" width="63%">
Gets the actual device stream index translated from a friendly stream name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-removealleffects">RemoveAllEffects</a>
</td>
<td align="left" width="63%">
Removes all effects from a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-removeeffect">RemoveEffect</a>
</td>
<td align="left" width="63%">
Removes an effect from a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-setcurrentdevicemediatype">SetCurrentDeviceMediaType</a>
</td>
<td align="left" width="63%">
Sets the output format for a capture stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-setmirrorstate">SetMirrorState</a>
</td>
<td align="left" width="63%">
Enables or disables mirroring of the video preview stream.

</td>
</tr>
</table> 


## -remarks



To get a pointer to the capture source, call <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-getsource">IMFCaptureEngine::GetSource</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

