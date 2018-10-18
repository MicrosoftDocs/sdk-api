---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.GetRotation
title: IMFCapturePreviewSink::GetRotation
author: windows-sdk-content
description: Gets the rotation of the video preview stream.
old-location: mf\imfcapturepreviewsink_getrotation.htm
tech.root: medfound
ms.assetid: 5C750060-762B-42EE-92AD-8497B83E5D51
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetRotation, GetRotation method [Media Foundation], GetRotation method [Media Foundation],IMFCapturePreviewSink interface, IMFCapturePreviewSink interface [Media Foundation],GetRotation method, IMFCapturePreviewSink.GetRotation, IMFCapturePreviewSink::GetRotation, mf.imfcapturepreviewsink_getrotation, mfcaptureengine/IMFCapturePreviewSink::GetRotation
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
 - mfcaptureengine.h
api_name:
 - IMFCapturePreviewSink.GetRotation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCapturePreviewSink::GetRotation


## -description


Gets the rotation of the video preview stream.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream. You must specify a video stream.


### -param pdwRotationValue [out]

Receives the image rotation, in degrees.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5E64C24D-D6EC-419B-9DC8-309EBCE0077E">IMFCapturePreviewSink</a>
 

 

