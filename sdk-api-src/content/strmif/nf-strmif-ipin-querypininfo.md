---
UID: NF:strmif.IPin.QueryPinInfo
title: IPin::QueryPinInfo (strmif.h)
description: The QueryPinInfo method retrieves information about the pin.
helpviewer_keywords: ["IPin interface [DirectShow]","QueryPinInfo method","IPin.QueryPinInfo","IPin::QueryPinInfo","IPinQueryPinInfo","QueryPinInfo","QueryPinInfo method [DirectShow]","QueryPinInfo method [DirectShow]","IPin interface","dshow.ipin_querypininfo","strmif/IPin::QueryPinInfo"]
old-location: dshow\ipin_querypininfo.htm
tech.root: dshow
ms.assetid: 1a7c85ce-46f1-4928-9e2a-3a4bd96dc771
ms.date: 4/26/2023
ms.keywords: IPin interface [DirectShow],QueryPinInfo method, IPin.QueryPinInfo, IPin::QueryPinInfo, IPinQueryPinInfo, QueryPinInfo, QueryPinInfo method [DirectShow], QueryPinInfo method [DirectShow],IPin interface, dshow.ipin_querypininfo, strmif/IPin::QueryPinInfo
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
 - IPin::QueryPinInfo
 - strmif/IPin::QueryPinInfo
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
 - IPin.QueryPinInfo
---

# IPin::QueryPinInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>QueryPinInfo</code> method retrieves information about the pin.

## -parameters

### -param pInfo [out]

Pointer to a [PIN_INFO](/windows/desktop/api/strmif/ns-strmif-pin_info) structure that receives the pin information.

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
</table>

## -remarks

When the method returns, if the <b>pFilter</b> member of the PIN_INFO structure is non-<b>NULL</b>, it has an outstanding reference count. Be sure to release the interface when you are done.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>