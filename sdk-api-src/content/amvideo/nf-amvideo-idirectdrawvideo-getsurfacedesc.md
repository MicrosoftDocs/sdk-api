---
UID: NF:amvideo.IDirectDrawVideo.GetSurfaceDesc
title: IDirectDrawVideo::GetSurfaceDesc (amvideo.h)
description: The GetSurfaceDesc method retrieves a DDSURFACEDESC structure describing the current DirectDraw surface.
helpviewer_keywords: ["GetSurfaceDesc","GetSurfaceDesc method [DirectShow]","GetSurfaceDesc method [DirectShow]","IDirectDrawVideo interface","IDirectDrawVideo interface [DirectShow]","GetSurfaceDesc method","IDirectDrawVideo.GetSurfaceDesc","IDirectDrawVideo::GetSurfaceDesc","IDirectDrawVideoGetSurfaceDesc","amvideo/IDirectDrawVideo::GetSurfaceDesc","dshow.idirectdrawvideo_getsurfacedesc"]
old-location: dshow\idirectdrawvideo_getsurfacedesc.htm
tech.root: dshow
ms.assetid: f3884dbf-c75c-45f7-953c-bfdc14734820
ms.date: 12/05/2018
ms.keywords: GetSurfaceDesc, GetSurfaceDesc method [DirectShow], GetSurfaceDesc method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetSurfaceDesc method, IDirectDrawVideo.GetSurfaceDesc, IDirectDrawVideo::GetSurfaceDesc, IDirectDrawVideoGetSurfaceDesc, amvideo/IDirectDrawVideo::GetSurfaceDesc, dshow.idirectdrawvideo_getsurfacedesc
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawVideo::GetSurfaceDesc
 - amvideo/IDirectDrawVideo::GetSurfaceDesc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDirectDrawVideo.GetSurfaceDesc
---

# IDirectDrawVideo::GetSurfaceDesc


## -description

The <code>GetSurfaceDesc</code> method retrieves a <b>DDSURFACEDESC</b> structure describing the current DirectDraw surface.

## -parameters

### -param pSurfaceDesc

Pointer to a <b>DDSURFACEDESC</b> structure describing the current DirectDraw surface.

## -returns

Returns an <b>HRESULT</b> value. If no surface has been allocated, this method will return E_FAIL. If a DCI primary surface is in use, the <b>DDSURFACEDESC</b> structure will not be filled in and the call will return S_FALSE.

## -remarks

Surfaces are allocated only when the renderer is paused. After the renderer has been paused, it cannot release the surfaces when stopped.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>