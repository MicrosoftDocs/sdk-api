---
UID: NF:strmif.IMemInputPin.GetAllocator
title: IMemInputPin::GetAllocator (strmif.h)
description: The GetAllocator method retrieves the memory allocator proposed by this pin. After the allocator has been selected, this method returns a pointer to the selected allocator.
helpviewer_keywords: ["GetAllocator","GetAllocator method [DirectShow]","GetAllocator method [DirectShow]","IMemInputPin interface","IMemInputPin interface [DirectShow]","GetAllocator method","IMemInputPin.GetAllocator","IMemInputPin::GetAllocator","IMemInputPinGetAllocator","dshow.imeminputpin_getallocator","strmif/IMemInputPin::GetAllocator"]
old-location: dshow\imeminputpin_getallocator.htm
tech.root: dshow
ms.assetid: ab49028e-ae27-4d4e-a5f1-a086ade25c5e
ms.date: 4/26/2023
ms.keywords: GetAllocator, GetAllocator method [DirectShow], GetAllocator method [DirectShow],IMemInputPin interface, IMemInputPin interface [DirectShow],GetAllocator method, IMemInputPin.GetAllocator, IMemInputPin::GetAllocator, IMemInputPinGetAllocator, dshow.imeminputpin_getallocator, strmif/IMemInputPin::GetAllocator
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
 - IMemInputPin::GetAllocator
 - strmif/IMemInputPin::GetAllocator
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
 - IMemInputPin.GetAllocator
---

# IMemInputPin::GetAllocator


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAllocator</code> method retrieves the memory allocator proposed by this pin. After the allocator has been selected, this method returns a pointer to the selected allocator.

## -parameters

### -param ppAllocator [out]

Receives a pointer to the allocator's <a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> interface. The caller must release the interface.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_ALLOCATOR</b></dt>
</dl>
</td>
<td width="60%">
No allocator is available.

</td>
</tr>
</table>

## -remarks

When an output pin connects to an input pin, it negotiates with the input pin to decide on a memory allocator. The output pin calls this method to retrieve the input pin's proposed allocator. It calls the <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-notifyallocator">IMemInputPin::NotifyAllocator</a> method to specify which allocator it selected.

If this method succeeds, the <b>IMemAllocator</b> interface has an outstanding reference count. Be sure to release it when you are done.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin Interface</a>