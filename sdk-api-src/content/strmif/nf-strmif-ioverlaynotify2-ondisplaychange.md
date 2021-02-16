---
UID: NF:strmif.IOverlayNotify2.OnDisplayChange
title: IOverlayNotify2::OnDisplayChange (strmif.h)
description: The OnDisplayChange method provides notification that the exposed window area has changed.
helpviewer_keywords: ["IOverlayNotify2 interface [DirectShow]","OnDisplayChange method","IOverlayNotify2.OnDisplayChange","IOverlayNotify2::OnDisplayChange","IOverlayNotify2OnDisplayChange","OnDisplayChange","OnDisplayChange method [DirectShow]","OnDisplayChange method [DirectShow]","IOverlayNotify2 interface","dshow.ioverlaynotify2_ondisplaychange","strmif/IOverlayNotify2::OnDisplayChange"]
old-location: dshow\ioverlaynotify2_ondisplaychange.htm
tech.root: dshow
ms.assetid: 8f32a373-5d98-4491-8bfb-9445cb15ff10
ms.date: 12/05/2018
ms.keywords: IOverlayNotify2 interface [DirectShow],OnDisplayChange method, IOverlayNotify2.OnDisplayChange, IOverlayNotify2::OnDisplayChange, IOverlayNotify2OnDisplayChange, OnDisplayChange, OnDisplayChange method [DirectShow], OnDisplayChange method [DirectShow],IOverlayNotify2 interface, dshow.ioverlaynotify2_ondisplaychange, strmif/IOverlayNotify2::OnDisplayChange
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
 - IOverlayNotify2::OnDisplayChange
 - strmif/IOverlayNotify2::OnDisplayChange
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
 - IOverlayNotify2.OnDisplayChange
---

# IOverlayNotify2::OnDisplayChange


## -description

The <code>OnDisplayChange</code> method provides notification that the exposed window area has changed.

## -parameters

### -param hMonitor [in]

Handle to the monitor used for displaying the overlay.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify2">IOverlayNotify2 Interface</a>