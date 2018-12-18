---
UID: NF:mfcaptureengine.IMFCaptureSource.GetDeviceStreamCategory
title: IMFCaptureSource::GetDeviceStreamCategory
author: windows-sdk-content
description: Gets the stream category for the specified source stream index.
old-location: mf\imfcapturesource_getdevicestreamcategory.htm
tech.root: medfound
ms.assetid: f3caa002-8676-44d3-9696-da5b0db09d9e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDeviceStreamCategory, GetDeviceStreamCategory method [Media Foundation], GetDeviceStreamCategory method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetDeviceStreamCategory method, IMFCaptureSource.GetDeviceStreamCategory, IMFCaptureSource::GetDeviceStreamCategory, mf.imfcapturesource_getdevicestreamcategory, mfcaptureengine/IMFCaptureSource::GetDeviceStreamCategory
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
 - IMFCaptureSource.GetDeviceStreamCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSource::GetDeviceStreamCategory


## -description


Gets the stream category for the specified source stream index.


## -parameters




### -param dwSourceStreamIndex [in]

The index of the source stream.


### -param pStreamCategory [out]

Receives the MF_CAPTURE_ENGINE_STREAM_CATEGORY of the specified source stream.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a>
 

 

