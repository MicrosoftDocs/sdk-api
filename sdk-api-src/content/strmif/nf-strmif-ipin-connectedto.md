---
UID: NF:strmif.IPin.ConnectedTo
title: IPin::ConnectedTo (strmif.h)
description: The ConnectedTo method retrieves a pointer to the connected pin, if any.
helpviewer_keywords: ["ConnectedTo","ConnectedTo method [DirectShow]","ConnectedTo method [DirectShow]","IPin interface","IPin interface [DirectShow]","ConnectedTo method","IPin.ConnectedTo","IPin::ConnectedTo","IPinConnectedTo","dshow.ipin_connectedto","strmif/IPin::ConnectedTo"]
old-location: dshow\ipin_connectedto.htm
tech.root: dshow
ms.assetid: 970c814f-2309-481e-9e8e-9bd32b83fdc7
ms.date: 4/26/2023
ms.keywords: ConnectedTo, ConnectedTo method [DirectShow], ConnectedTo method [DirectShow],IPin interface, IPin interface [DirectShow],ConnectedTo method, IPin.ConnectedTo, IPin::ConnectedTo, IPinConnectedTo, dshow.ipin_connectedto, strmif/IPin::ConnectedTo
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
 - IPin::ConnectedTo
 - strmif/IPin::ConnectedTo
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
 - IPin.ConnectedTo
---

# IPin::ConnectedTo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ConnectedTo</b> method retrieves a pointer to the connected pin, if any.

## -parameters

### -param pPin [out]

Receives a pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of the other pin. The caller must release the interface. This parameter cannot be <b>NULL</b>.

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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Pin is not connected.

</td>
</tr>
</table>

## -remarks

If the method succeeds, the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface that it returns has an outstanding reference count. Be sure to release it when you are done.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/find-an-unconnected-pin-on-a-filter">Find an Unconnected Pin on a Filter</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>