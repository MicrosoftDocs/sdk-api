---
UID: NF:strmif.IOverlay.GetWindowHandle
title: IOverlay::GetWindowHandle (strmif.h)
description: The GetWindowHandle method retrieves the current window handle.
helpviewer_keywords: ["GetWindowHandle","GetWindowHandle method [DirectShow]","GetWindowHandle method [DirectShow]","IOverlay interface","IOverlay interface [DirectShow]","GetWindowHandle method","IOverlay.GetWindowHandle","IOverlay::GetWindowHandle","IOverlayGetWindowHandle","dshow.ioverlay_getwindowhandle","strmif/IOverlay::GetWindowHandle"]
old-location: dshow\ioverlay_getwindowhandle.htm
tech.root: dshow
ms.assetid: f2d4cc53-ab0a-4c15-9818-3f312a13d4e1
ms.date: 12/05/2018
ms.keywords: GetWindowHandle, GetWindowHandle method [DirectShow], GetWindowHandle method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],GetWindowHandle method, IOverlay.GetWindowHandle, IOverlay::GetWindowHandle, IOverlayGetWindowHandle, dshow.ioverlay_getwindowhandle, strmif/IOverlay::GetWindowHandle
req.header: strmif.h
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
 - IOverlay::GetWindowHandle
 - strmif/IOverlay::GetWindowHandle
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
 - IOverlay.GetWindowHandle
---

# IOverlay::GetWindowHandle


## -description

The <code>GetWindowHandle</code> method retrieves the current window handle.

## -parameters

### -param pHwnd [out]

Receives the window handle.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>