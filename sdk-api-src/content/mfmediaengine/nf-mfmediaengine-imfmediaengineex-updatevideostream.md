---
UID: NF:mfmediaengine.IMFMediaEngineEx.UpdateVideoStream
title: IMFMediaEngineEx::UpdateVideoStream (mfmediaengine.h)
description: Updates the source rectangle, destination rectangle, and border color for the video.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","UpdateVideoStream method","IMFMediaEngineEx.UpdateVideoStream","IMFMediaEngineEx::UpdateVideoStream","UpdateVideoStream","UpdateVideoStream method [Media Foundation]","UpdateVideoStream method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_updatevideostream","mfmediaengine/IMFMediaEngineEx::UpdateVideoStream"]
old-location: mf\imfmediaengineex_updatevideostream.htm
tech.root: mf
ms.assetid: 2A9EB449-ED76-4E2C-BC55-20E134B43B43
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],UpdateVideoStream method, IMFMediaEngineEx.UpdateVideoStream, IMFMediaEngineEx::UpdateVideoStream, UpdateVideoStream, UpdateVideoStream method [Media Foundation], UpdateVideoStream method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_updatevideostream, mfmediaengine/IMFMediaEngineEx::UpdateVideoStream
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineEx::UpdateVideoStream
 - mfmediaengine/IMFMediaEngineEx::UpdateVideoStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.UpdateVideoStream
---

# IMFMediaEngineEx::UpdateVideoStream


## -description

Updates the source rectangle, destination rectangle, and border color for the video.

## -parameters

### -param pSrc [in]

A pointer to an <a href="/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect">MFVideoNormalizedRect</a> structure that specifies the source rectangle. The source rectangle defines the area of the video frame that is displayed. If this parameter is <b>NULL</b>, the entire video frame is displayed.

### -param pDst [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the destination rectangle. The destination rectangle defines the area of the window or DirectComposition visual where the video is drawn.

### -param pBorderClr [in]

A pointer to an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a> structure that specifies the border color.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In rendering mode, call this method to reposition the video, update the border color, or repaint the video frame. If all of the parameters are <b>NULL</b>, the method repaints the most recent video frame.

In frame-server mode, this method has no effect.

See <a href="/windows/desktop/medfound/video-processor-mft">Video Processor MFT</a> for info regarding source and destination rectangles in the <b>Video Processor MFT</b>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>