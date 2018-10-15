---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.SetRenderSurface
title: IMFCapturePreviewSink::SetRenderSurface
author: windows-sdk-content
description: Specifies a Microsoft DirectComposition visual for preview.
old-location: mf\imfcapturepreviewsink_setrendersurface.htm
tech.root: medfound
ms.assetid: AC50EB86-A39D-4ACA-9582-A8DB0232E056
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],SetRenderSurface method, IMFCapturePreviewSink.SetRenderSurface, IMFCapturePreviewSink::SetRenderSurface, SetRenderSurface, SetRenderSurface method [Media Foundation], SetRenderSurface method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_setrendersurface, mfcaptureengine/IMFCapturePreviewSink::SetRenderSurface
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
 - IMFCapturePreviewSink.SetRenderSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCapturePreviewSink::SetRenderSurface


## -description


Specifies a Microsoft DirectComposition visual for preview.


## -parameters




### -param pSurface [in]

A pointer to a DirectComposition visual that implements the <a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5E64C24D-D6EC-419B-9DC8-309EBCE0077E">IMFCapturePreviewSink</a>
 

 

