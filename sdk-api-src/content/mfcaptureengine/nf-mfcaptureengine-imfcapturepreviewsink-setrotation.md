---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.SetRotation
title: IMFCapturePreviewSink::SetRotation
author: windows-driver-content
description: Rotates the video preview stream.
old-location: mf\imfcapturepreviewsink_setrotation.htm
old-project: medfound
ms.assetid: 84C53A34-B2FB-4D13-9A45-5172E9E3CEE8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],SetRotation method, IMFCapturePreviewSink.SetRotation, IMFCapturePreviewSink::SetRotation, SetRotation, SetRotation method [Media Foundation], SetRotation method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_setrotation, mfcaptureengine/IMFCapturePreviewSink::SetRotation
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
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfcaptureengine.h
api_name:
-	IMFCapturePreviewSink.SetRotation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCapturePreviewSink::SetRotation


## -description


Rotates the video preview stream.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream to rotate. You must specify a video stream.


### -param dwRotationValue [in]

The amount to rotate the video, in degrees. Valid values are 0, 90, 180, and 270. The value zero restores the video to its original orientation.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5E64C24D-D6EC-419B-9DC8-309EBCE0077E">IMFCapturePreviewSink</a>
 

 

