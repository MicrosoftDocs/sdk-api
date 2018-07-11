---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.GetRotation
title: IMFCaptureRecordSink::GetRotation
author: windows-sdk-content
description: Gets the rotation that is currently being applied to the recorded video stream.
old-location: mf\imfcapturerecordsink_getrotation.htm
old-project: medfound
ms.assetid: E582ED9C-D7B8-4DF9-B72F-361E682DB93F
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRotation, GetRotation method [Media Foundation], GetRotation method [Media Foundation],IMFCaptureRecordSink interface, IMFCaptureRecordSink interface [Media Foundation],GetRotation method, IMFCaptureRecordSink.GetRotation, IMFCaptureRecordSink::GetRotation, mf.imfcapturerecordsink_getrotation, mfcaptureengine/IMFCaptureRecordSink::GetRotation
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureRecordSink.GetRotation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureRecordSink::GetRotation


## -description


Gets the rotation that is currently being applied to the recorded video stream.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream. You must specify a video stream.


### -param pdwRotationValue [out]

Receives the image rotation, in degrees.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/AEF5923D-C4ED-4BEA-A969-163ED837A5BD">IMFCaptureRecordSink</a>
 

 

