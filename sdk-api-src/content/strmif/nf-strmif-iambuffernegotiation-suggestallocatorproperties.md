---
UID: NF:strmif.IAMBufferNegotiation.SuggestAllocatorProperties
title: IAMBufferNegotiation::SuggestAllocatorProperties (strmif.h)
description: The SuggestAllocatorProperties method informs the pin of the application's preferred allocator properties. Call this method before the pin connects.
helpviewer_keywords: ["IAMBufferNegotiation interface [DirectShow]","SuggestAllocatorProperties method","IAMBufferNegotiation.SuggestAllocatorProperties","IAMBufferNegotiation::SuggestAllocatorProperties","IAMBufferNegotiationSuggestAllocatorProperties","SuggestAllocatorProperties","SuggestAllocatorProperties method [DirectShow]","SuggestAllocatorProperties method [DirectShow]","IAMBufferNegotiation interface","dshow.iambuffernegotiation_suggestallocatorproperties","strmif/IAMBufferNegotiation::SuggestAllocatorProperties"]
old-location: dshow\iambuffernegotiation_suggestallocatorproperties.htm
tech.root: dshow
ms.assetid: f6a7f2c4-be8b-4721-87f4-274ba365784f
ms.date: 4/26/2023
ms.keywords: IAMBufferNegotiation interface [DirectShow],SuggestAllocatorProperties method, IAMBufferNegotiation.SuggestAllocatorProperties, IAMBufferNegotiation::SuggestAllocatorProperties, IAMBufferNegotiationSuggestAllocatorProperties, SuggestAllocatorProperties, SuggestAllocatorProperties method [DirectShow], SuggestAllocatorProperties method [DirectShow],IAMBufferNegotiation interface, dshow.iambuffernegotiation_suggestallocatorproperties, strmif/IAMBufferNegotiation::SuggestAllocatorProperties
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
 - IAMBufferNegotiation::SuggestAllocatorProperties
 - strmif/IAMBufferNegotiation::SuggestAllocatorProperties
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
 - IAMBufferNegotiation.SuggestAllocatorProperties
---

# IAMBufferNegotiation::SuggestAllocatorProperties


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SuggestAllocatorProperties</code> method informs the pin of the application's preferred allocator properties. Call this method before the pin connects.

## -parameters

### -param pprop [in]

Pointer to an [ALLOCATOR_PROPERTIES](/windows/desktop/api/strmif/ns-strmif-allocator_properties) structure that contains the requested properties. A negative value for any member indicates that the pin should use its default setting for that property.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Pin is already connected.

</td>
</tr>
</table>

## -remarks

If both pins in the connection expose the <a href="/windows/desktop/api/strmif/nn-strmif-iambuffernegotiation">IAMBufferNegotiation</a> interface, call this method on each pin, to ensure that one pin does not override the other.

To request a particular number of buffers, set the <b>cBuffers</b> member of the <b>ALLOCATOR_PROPERTIES</b> structure. To request a particular buffer size, set the <b>cbBuffer</b> member. An application typically should not specify the alignment or prefix. If the number of buffers or size of each buffer is too small, the filter graph might drop samples.


#### Examples

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
ALLOCATOR_PROPERTIES AllocProp;
AllocProp.cbAlign = -1;  // -1 means no preference.
AllocProp.cbBuffer = dwBytesPerSec *  dwLatencyInMilliseconds / 1000;
AllocProp.cbPrefix = -1;
AllocProp.cBuffers = -1;
pIAMBufferNegotiation-&gt;SuggestAllocatorProperties(&amp;AllocProp);
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iambuffernegotiation">IAMBufferNegotiation Interface</a>