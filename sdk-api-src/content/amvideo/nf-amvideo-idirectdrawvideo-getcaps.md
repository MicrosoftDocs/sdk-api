---
UID: NF:amvideo.IDirectDrawVideo.GetCaps
title: IDirectDrawVideo::GetCaps (amvideo.h)
description: The GetCaps method retrieves a DirectDraw-defined DDCAPS structure containing the hardware capabilities.
helpviewer_keywords: ["GetCaps","GetCaps method [DirectShow]","GetCaps method [DirectShow]","IDirectDrawVideo interface","IDirectDrawVideo interface [DirectShow]","GetCaps method","IDirectDrawVideo.GetCaps","IDirectDrawVideo::GetCaps","IDirectDrawVideoGetCaps","amvideo/IDirectDrawVideo::GetCaps","dshow.idirectdrawvideo_getcaps"]
old-location: dshow\idirectdrawvideo_getcaps.htm
tech.root: dshow
ms.assetid: d63437e3-4e8a-49de-b555-db29d235569d
ms.date: 12/05/2018
ms.keywords: GetCaps, GetCaps method [DirectShow], GetCaps method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetCaps method, IDirectDrawVideo.GetCaps, IDirectDrawVideo::GetCaps, IDirectDrawVideoGetCaps, amvideo/IDirectDrawVideo::GetCaps, dshow.idirectdrawvideo_getcaps
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
 - IDirectDrawVideo::GetCaps
 - amvideo/IDirectDrawVideo::GetCaps
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
 - IDirectDrawVideo.GetCaps
---

# IDirectDrawVideo::GetCaps


## -description

The <code>GetCaps</code> method retrieves a DirectDraw-defined DDCAPS structure containing the hardware capabilities.

## -parameters

### -param pCaps

Pointer to a DDCAPS structure containing the hardware capabilities.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

If the renderer has not loaded DirectDraw, this method returns E_FAIL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>