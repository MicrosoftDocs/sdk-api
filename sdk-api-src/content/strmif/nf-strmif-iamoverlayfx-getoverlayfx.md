---
UID: NF:strmif.IAMOverlayFX.GetOverlayFX
title: IAMOverlayFX::GetOverlayFX (strmif.h)
description: The GetOverlayFX method retrieves the effects currently applied to the overlay surface, if any. The application can call this method while the filter graph is running.
helpviewer_keywords: ["GetOverlayFX","GetOverlayFX method [DirectShow]","GetOverlayFX method [DirectShow]","IAMOverlayFX interface","IAMOverlayFX interface [DirectShow]","GetOverlayFX method","IAMOverlayFX.GetOverlayFX","IAMOverlayFX::GetOverlayFX","IAMOverlayFXGetOverlayFX","dshow.iamoverlayfx_getoverlayfx","strmif/IAMOverlayFX::GetOverlayFX"]
old-location: dshow\iamoverlayfx_getoverlayfx.htm
tech.root: dshow
ms.assetid: f8232fcf-a0d8-4155-941e-8613c09b4bbf
ms.date: 4/26/2023
ms.keywords: GetOverlayFX, GetOverlayFX method [DirectShow], GetOverlayFX method [DirectShow],IAMOverlayFX interface, IAMOverlayFX interface [DirectShow],GetOverlayFX method, IAMOverlayFX.GetOverlayFX, IAMOverlayFX::GetOverlayFX, IAMOverlayFXGetOverlayFX, dshow.iamoverlayfx_getoverlayfx, strmif/IAMOverlayFX::GetOverlayFX
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMOverlayFX::GetOverlayFX
 - strmif/IAMOverlayFX::GetOverlayFX
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
 - IAMOverlayFX.GetOverlayFX
---

# IAMOverlayFX::GetOverlayFX


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetOverlayFX</code> method retrieves the effects currently applied to the overlay surface, if any. The application can call this method while the filter graph is running.

## -parameters

### -param lpdwOverlayFX [out]

Pointer a variable that receives a value indicating which effects, if any, are currently applied to the overlay surface. The value is a logical combination of flags from the <a href="/windows/desktop/api/strmif/ne-strmif-amoverlayfx">AMOVERLAYFX</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns S_OK if successful, or E_POINTER to indicate a <b>NULL</b> pointer argument.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamoverlayfx">IAMOverlayFX Interface</a>