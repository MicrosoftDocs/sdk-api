---
UID: NF:strmif.IMemInputPin.NotifyAllocator
title: IMemInputPin::NotifyAllocator (strmif.h)
description: The NotifyAllocator method specifies an allocator for the connection.
helpviewer_keywords: ["IMemInputPin interface [DirectShow]","NotifyAllocator method","IMemInputPin.NotifyAllocator","IMemInputPin::NotifyAllocator","IMemInputPinNotifyAllocator","NotifyAllocator","NotifyAllocator method [DirectShow]","NotifyAllocator method [DirectShow]","IMemInputPin interface","dshow.imeminputpin_notifyallocator","strmif/IMemInputPin::NotifyAllocator"]
old-location: dshow\imeminputpin_notifyallocator.htm
tech.root: dshow
ms.assetid: dbc9c0ce-3e9c-4402-9d3e-1c7295e94ad9
ms.date: 4/26/2023
ms.keywords: IMemInputPin interface [DirectShow],NotifyAllocator method, IMemInputPin.NotifyAllocator, IMemInputPin::NotifyAllocator, IMemInputPinNotifyAllocator, NotifyAllocator, NotifyAllocator method [DirectShow], NotifyAllocator method [DirectShow],IMemInputPin interface, dshow.imeminputpin_notifyallocator, strmif/IMemInputPin::NotifyAllocator
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
 - IMemInputPin::NotifyAllocator
 - strmif/IMemInputPin::NotifyAllocator
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
 - IMemInputPin.NotifyAllocator
---

# IMemInputPin::NotifyAllocator


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>NotifyAllocator</code> method specifies an allocator for the connection.

## -parameters

### -param pAllocator [in]

Pointer to the allocator's <a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> interface.

### -param bReadOnly [out]

Flag that specifies whether samples from this allocator are read-only. If <b>TRUE</b>, samples are read-only.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin. The output pin might use the allocator that the input pin proposed in the <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-getallocator">IMemInputPin::GetAllocator</a> method, or it might provide its own allocator.

If the <i>bReadOnly</i> parameter is <b>TRUE</b>, all samples in the allocator are read-only. The filter must copy them to modify the data.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin Interface</a>