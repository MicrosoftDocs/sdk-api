---
UID: NF:strmif.IBaseFilter.FindPin
title: IBaseFilter::FindPin (strmif.h)
description: The FindPin method retrieves the pin with the specified identifier.
helpviewer_keywords: ["FindPin","FindPin method [DirectShow]","FindPin method [DirectShow]","IBaseFilter interface","IBaseFilter interface [DirectShow]","FindPin method","IBaseFilter.FindPin","IBaseFilter::FindPin","IBaseFilterFindPin","dshow.ibasefilter_findpin","strmif/IBaseFilter::FindPin"]
old-location: dshow\ibasefilter_findpin.htm
tech.root: dshow
ms.assetid: 0bdefaeb-f631-4b79-9965-c1c570e0ff80
ms.date: 4/26/2023
ms.keywords: FindPin, FindPin method [DirectShow], FindPin method [DirectShow],IBaseFilter interface, IBaseFilter interface [DirectShow],FindPin method, IBaseFilter.FindPin, IBaseFilter::FindPin, IBaseFilterFindPin, dshow.ibasefilter_findpin, strmif/IBaseFilter::FindPin
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
 - IBaseFilter::FindPin
 - strmif/IBaseFilter::FindPin
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
 - IBaseFilter.FindPin
---

# IBaseFilter::FindPin


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>FindPin</code> method retrieves the pin with the specified identifier.

## -parameters

### -param Id [in]

Pointer to a constant wide-character string that identifies the pin. Call the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-queryid">IPin::QueryId</a> method to retrieve a pin's identifier.

### -param ppPin [out]

Address of a variable that receives a pointer to the pin's <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface. If the method fails, <i>*ppPin</i> is set to <b>NULL</b>.

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
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find a pin with this identifier.

</td>
</tr>
</table>

## -remarks

This method supports graph persistence. Use the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-queryid">IPin::QueryId</a> method to save a pin's state, and use this method to restore the state. The pin's identifier string is defined by the filter implementation. The identifier must be unique within the filter.

If the method succeeds, the <b>IPin</b> interface that it returns has an outstanding reference count. Be sure to release the interface when you are done.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter Interface</a>