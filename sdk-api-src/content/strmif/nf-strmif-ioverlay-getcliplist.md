---
UID: NF:strmif.IOverlay.GetClipList
title: IOverlay::GetClipList (strmif.h)
description: The GetClipList method retrieves the clipping list.
helpviewer_keywords: ["GetClipList","GetClipList method [DirectShow]","GetClipList method [DirectShow]","IOverlay interface","IOverlay interface [DirectShow]","GetClipList method","IOverlay.GetClipList","IOverlay::GetClipList","IOverlayGetClipList","dshow.ioverlay_getcliplist","strmif/IOverlay::GetClipList"]
old-location: dshow\ioverlay_getcliplist.htm
tech.root: dshow
ms.assetid: 3133bcae-0a08-45e9-b70a-07ea6ffef8ee
ms.date: 4/26/2023
ms.keywords: GetClipList, GetClipList method [DirectShow], GetClipList method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],GetClipList method, IOverlay.GetClipList, IOverlay::GetClipList, IOverlayGetClipList, dshow.ioverlay_getcliplist, strmif/IOverlay::GetClipList
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
 - IOverlay::GetClipList
 - strmif/IOverlay::GetClipList
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
 - IOverlay.GetClipList
---

# IOverlay::GetClipList


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetClipList</code> method retrieves the clipping list.

## -parameters

### -param pSourceRect [out]

Pointer to the bounding client rectangle.

### -param pDestinationRect [in]

Pointer to the destination rectangle.

### -param ppRgnData [out]

Address of a pointer to the header and data describing clipping. If successful, free the allocated memory by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay</a> implementation allocates the memory for the clipping rectangles, because it can vary in length. The filter calling this method should free the memory (using <b>CoTaskMemFree</b>) when it is finished with it.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>