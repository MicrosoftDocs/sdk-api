---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.SetRenderSurface
title: IMFCapturePreviewSink::SetRenderSurface (mfcaptureengine.h)
description: Specifies a Microsoft DirectComposition visual for preview.
helpviewer_keywords: ["IMFCapturePreviewSink interface [Media Foundation]","SetRenderSurface method","IMFCapturePreviewSink.SetRenderSurface","IMFCapturePreviewSink::SetRenderSurface","SetRenderSurface","SetRenderSurface method [Media Foundation]","SetRenderSurface method [Media Foundation]","IMFCapturePreviewSink interface","mf.imfcapturepreviewsink_setrendersurface","mfcaptureengine/IMFCapturePreviewSink::SetRenderSurface"]
old-location: mf\imfcapturepreviewsink_setrendersurface.htm
tech.root: mf
ms.assetid: AC50EB86-A39D-4ACA-9582-A8DB0232E056
ms.date: 12/05/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],SetRenderSurface method, IMFCapturePreviewSink.SetRenderSurface, IMFCapturePreviewSink::SetRenderSurface, SetRenderSurface, SetRenderSurface method [Media Foundation], SetRenderSurface method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_setrendersurface, mfcaptureengine/IMFCapturePreviewSink::SetRenderSurface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFCapturePreviewSink::SetRenderSurface
 - mfcaptureengine/IMFCapturePreviewSink::SetRenderSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCapturePreviewSink.SetRenderSurface
---

# IMFCapturePreviewSink::SetRenderSurface


## -description

Specifies a Microsoft DirectComposition visual for preview.

## -parameters

### -param pSurface [in]

A pointer to a DirectComposition visual that implements the <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink">IMFCapturePreviewSink</a>