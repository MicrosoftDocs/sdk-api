---
UID: NF:strmif.IPin.QueryInternalConnections
title: IPin::QueryInternalConnections (strmif.h)
description: The QueryInternalConnections method retrieves the pins that are connected internally to this pin (within the filter).
helpviewer_keywords: ["IPin interface [DirectShow]","QueryInternalConnections method","IPin.QueryInternalConnections","IPin::QueryInternalConnections","IPinQueryInternalConnections","QueryInternalConnections","QueryInternalConnections method [DirectShow]","QueryInternalConnections method [DirectShow]","IPin interface","dshow.ipin_queryinternalconnections","strmif/IPin::QueryInternalConnections"]
old-location: dshow\ipin_queryinternalconnections.htm
tech.root: dshow
ms.assetid: c0289b89-9220-402c-858c-09076e2ab6b6
ms.date: 4/26/2023
ms.keywords: IPin interface [DirectShow],QueryInternalConnections method, IPin.QueryInternalConnections, IPin::QueryInternalConnections, IPinQueryInternalConnections, QueryInternalConnections, QueryInternalConnections method [DirectShow], QueryInternalConnections method [DirectShow],IPin interface, dshow.ipin_queryinternalconnections, strmif/IPin::QueryInternalConnections
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
 - IPin::QueryInternalConnections
 - strmif/IPin::QueryInternalConnections
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
 - IPin.QueryInternalConnections
---

# IPin::QueryInternalConnections


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>QueryInternalConnections</b> method retrieves the pins that are connected internally to this pin (within the filter).

## -parameters

### -param apPin [out]

Address of an array of <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> pointers. The caller allocates the array. The method fills the array with <b>IPin</b> pointers. If <i>nPin</i> is zero, this parameter can be <b>NULL</b>.

### -param nPin [in, out]

On input, specifies the size of the array. On output, specifies the number of internally connected pins.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Insufficient array size.

</td>
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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

## -remarks

This method returns information about the filter's internal mapping of input pins to output pins. In other words, it describes how the input pins deliver data to the output pins.

In most filters, every input pin connects to every output pin. For example, in a transform filter, one input connects to one output; in a splitter filter, one input connects to multiple outputs. In these cases, the method should simply return E_NOTIMPL.

Otherwise, the method returns an array of <b>IPin</b> pointers, one for each pin that is mapped internally to the pin you have queried. If you call the method on an input pin, the array contains pointers to output pins, and vice versa.

The caller allocates the array of <b>IPin</b> pointers. To get the required array size, call the method once with <i>apPin</i> equal to <b>NULL</b>. The size is returned in the <i>nPin</i> parameter. Then allocate the array and call the method again, setting <i>apPin</i> equal to the address of the array and <i>nPin</i> equal to the array size. The method then fills the array with <b>IPin</b> pointers. Each returned pointer has an outstanding reference count and must be released by the caller.

This method has another use that is now deprecated: The <a href="/windows/desktop/DirectShow/filter-graph-manager">Filter Graph Manager</a> treats a filter as being a renderer filter if at least one input pin implements this method but returns zero in <i>nPin</i>. If you are writing a new renderer filter, however, you should implement the <a href="/windows/desktop/api/strmif/nn-strmif-iamfiltermiscflags">IAMFilterMiscFlags</a> interface instead of using this method to indicate that the filter is a renderer.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>