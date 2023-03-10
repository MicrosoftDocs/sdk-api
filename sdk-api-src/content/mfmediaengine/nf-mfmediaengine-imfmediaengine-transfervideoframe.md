---
UID: NF:mfmediaengine.IMFMediaEngine.TransferVideoFrame
title: IMFMediaEngine::TransferVideoFrame (mfmediaengine.h)
description: Copies the current video frame to a DXGI surface or WIC bitmap.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","TransferVideoFrame method","IMFMediaEngine.TransferVideoFrame","IMFMediaEngine::TransferVideoFrame","TransferVideoFrame","TransferVideoFrame method [Media Foundation]","TransferVideoFrame method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_transfervideoframe","mfmediaengine/IMFMediaEngine::TransferVideoFrame"]
old-location: mf\imfmediaengine_transfervideoframe.htm
tech.root: mf
ms.assetid: 07DB29E2-9F09-46CB-B138-197D95EC37F0
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],TransferVideoFrame method, IMFMediaEngine.TransferVideoFrame, IMFMediaEngine::TransferVideoFrame, TransferVideoFrame, TransferVideoFrame method [Media Foundation], TransferVideoFrame method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_transfervideoframe, mfmediaengine/IMFMediaEngine::TransferVideoFrame
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
 - IMFMediaEngine::TransferVideoFrame
 - mfmediaengine/IMFMediaEngine::TransferVideoFrame
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
 - IMFMediaEngine.TransferVideoFrame
---

# IMFMediaEngine::TransferVideoFrame


## -description

Copies the current video frame to a DXGI surface or WIC bitmap.

## -parameters

### -param pDstSurf [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the destination surface.

### -param pSrc [in]

A pointer to an <a href="/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect">MFVideoNormalizedRect</a> structure that specifies the source rectangle.

### -param pDst [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the destination rectangle.

### -param pBorderClr [in]

A pointer to an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a> structure that specifies the border color.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In frame-server mode, call this method to blit the video frame to a DXGI or WIC surface. The application can call this method at any time after the Media Engine loads a video resource. Typically, however, the application calls <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-onvideostreamtick">IMFMediaEngine::OnVideoStreamTick</a> first, to determine whether a new frame is available. If <b>OnVideoStreamTick</b> returns <b>S_OK</b>, the application then calls <b>TransferVideoFrame</b>.

The Media Engine scales and letterboxes the video to fit the destination rectangle. It fills the letterbox area with the border color.

For protected content, call the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-transfervideoframe">IMFMediaEngineProtectedContent::TransferVideoFrame</a> method instead of this method.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>