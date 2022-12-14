---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.UpdateVideo
title: IMFCapturePreviewSink::UpdateVideo (mfcaptureengine.h)
description: Updates the video frame. (IMFCapturePreviewSink.UpdateVideo)
helpviewer_keywords: ["IMFCapturePreviewSink interface [Media Foundation]","UpdateVideo method","IMFCapturePreviewSink.UpdateVideo","IMFCapturePreviewSink::UpdateVideo","UpdateVideo","UpdateVideo method [Media Foundation]","UpdateVideo method [Media Foundation]","IMFCapturePreviewSink interface","mf.imfcapturepreviewsink_updatevideo","mfcaptureengine/IMFCapturePreviewSink::UpdateVideo"]
old-location: mf\imfcapturepreviewsink_updatevideo.htm
tech.root: mf
ms.assetid: B541D209-BB03-4FCF-834C-82002037C357
ms.date: 12/05/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],UpdateVideo method, IMFCapturePreviewSink.UpdateVideo, IMFCapturePreviewSink::UpdateVideo, UpdateVideo, UpdateVideo method [Media Foundation], UpdateVideo method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_updatevideo, mfcaptureengine/IMFCapturePreviewSink::UpdateVideo
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
 - IMFCapturePreviewSink::UpdateVideo
 - mfcaptureengine/IMFCapturePreviewSink::UpdateVideo
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
 - IMFCapturePreviewSink.UpdateVideo
---

# IMFCapturePreviewSink::UpdateVideo


## -description

Updates the video frame.  Call this method when the preview window receives a <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> or <a href="/windows/desktop/winmsg/wm-size">WM_SIZE</a> message.

## -parameters

### -param pSrc [in]

A pointer to an <a href="/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect">MFVideoNormalizedRect</a> structure that specifies the source rectangle. The source rectangle defines the area of the video frame that is displayed. If this parameter is <b>NULL</b>, the entire video frame is displayed.

### -param pDst [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the destination rectangle. The destination rectangle defines the area of the window or DirectComposition visual where the video is drawn.

### -param pBorderClr [in]

The border color. Use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro to create this value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink">IMFCapturePreviewSink</a>
