---
UID: NF:mfcaptureengine.IMFCapturePhotoSink.SetOutputFileName
title: IMFCapturePhotoSink::SetOutputFileName
author: windows-sdk-content
description: Specifies the name of the output file for the still image.
old-location: mf\imfcapturephotosink_setoutputfilename.htm
old-project: medfound
ms.assetid: CAA9F7CF-A92F-4039-BEA5-07A730E82EE4
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFCapturePhotoSink interface [Media Foundation],SetOutputFileName method, IMFCapturePhotoSink.SetOutputFileName, IMFCapturePhotoSink::SetOutputFileName, SetOutputFileName, SetOutputFileName method [Media Foundation], SetOutputFileName method [Media Foundation],IMFCapturePhotoSink interface, mf.imfcapturephotosink_setoutputfilename, mfcaptureengine/IMFCapturePhotoSink::SetOutputFileName
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
 - IMFCapturePhotoSink.SetOutputFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCapturePhotoSink::SetOutputFileName


## -description


Specifies the name of the output file for the still image.


## -parameters




### -param fileName [in]

A null-terminated string that contains the URL of the output file. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this method overrides any previous call to <a href="https://msdn.microsoft.com/D67C2D66-FC40-4AF3-9E83-29D0DBF99AD3">IMFCapturePhotoSink::SetOutputByteStream</a> or <a href="https://msdn.microsoft.com/595716F6-8059-4B56-9FB3-906846BA3CBB">IMFCapturePhotoSink::SetSampleCallback</a>.




## -see-also




<a href="https://msdn.microsoft.com/14BB9A86-47F2-4CFE-A932-3F2C7B6AF2BA">IMFCapturePhotoSink</a>
 

 

