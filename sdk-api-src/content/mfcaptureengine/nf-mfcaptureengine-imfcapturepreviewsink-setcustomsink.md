---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.SetCustomSink
title: IMFCapturePreviewSink::SetCustomSink (mfcaptureengine.h)
description: Sets a custom media sink for preview.helpviewer_keywords: ["IMFCapturePreviewSink interface [Media Foundation]","SetCustomSink method","IMFCapturePreviewSink.SetCustomSink","IMFCapturePreviewSink::SetCustomSink","SetCustomSink","SetCustomSink method [Media Foundation]","SetCustomSink method [Media Foundation]","IMFCapturePreviewSink interface","mf.imfcapturepreviewsink_setcustomsink","mfcaptureengine/IMFCapturePreviewSink::SetCustomSink"]
old-location: mf\imfcapturepreviewsink_setcustomsink.htm
tech.root: medfound
ms.assetid: 98D6F026-408F-4C22-B4A3-68C1B0EFD1E9
ms.date: 12/05/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],SetCustomSink method, IMFCapturePreviewSink.SetCustomSink, IMFCapturePreviewSink::SetCustomSink, SetCustomSink, SetCustomSink method [Media Foundation], SetCustomSink method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_setcustomsink, mfcaptureengine/IMFCapturePreviewSink::SetCustomSink
f1_keywords:
- mfcaptureengine/IMFCapturePreviewSink.SetCustomSink
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
- IMFCapturePreviewSink.SetCustomSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCapturePreviewSink::SetCustomSink


## -description


Sets a custom media sink for preview.


## -parameters




### -param pMediaSink [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface of the media sink.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method overrides the default selection of the media sink for preview.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink">IMFCapturePreviewSink</a>
 

 

