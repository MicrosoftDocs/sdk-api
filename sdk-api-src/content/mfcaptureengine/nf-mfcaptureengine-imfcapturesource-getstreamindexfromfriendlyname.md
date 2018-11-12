---
UID: NF:mfcaptureengine.IMFCaptureSource.GetStreamIndexFromFriendlyName
title: IMFCaptureSource::GetStreamIndexFromFriendlyName
author: windows-sdk-content
description: Gets the actual device stream index translated from a friendly stream name.
old-location: mf\imfcapturesource_getstreamindexfromfriendlyname.htm
tech.root: medfound
ms.assetid: 38bc2ca8-29ff-4a23-9b78-693aaab6767f
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetStreamIndexFromFriendlyName, GetStreamIndexFromFriendlyName method [Media Foundation], GetStreamIndexFromFriendlyName method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetStreamIndexFromFriendlyName method, IMFCaptureSource.GetStreamIndexFromFriendlyName, IMFCaptureSource::GetStreamIndexFromFriendlyName, mf.imfcapturesource_getstreamindexfromfriendlyname, mfcaptureengine/IMFCaptureSource::GetStreamIndexFromFriendlyName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - Mfcaptureengine.h
api_name:
 - IMFCaptureSource.GetStreamIndexFromFriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSource::GetStreamIndexFromFriendlyName


## -description


Gets the actual device stream index translated from a friendly stream name.


## -parameters




### -param uifriendlyName [in]

The friendly name.  Can be one of the following:

<ul>
<li>MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM</li>
<li>MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM</li>
<li>MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM</li>
<li>MF_CAPTURE_ENGINE_PREFERRED_SOURCE_VIDEO_STREAM_FOR_RECORD</li>
<li>MF_CAPTURE_ENGINE_PREFERRED_SOURCE_VIDEO_STREAM_FOR_PREVIEW</li>
<li>MF_CAPTURE_ENGINE_FIRST_SOURCE_INDEPENDENT_PHOTO_STREAM</li>
</ul>

### -param pdwActualStreamIndex [out]

Receives the value of the stream index that corresponds to the friendly name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a>
 

 

