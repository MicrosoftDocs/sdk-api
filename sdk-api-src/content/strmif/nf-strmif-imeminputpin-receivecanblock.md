---
UID: NF:strmif.IMemInputPin.ReceiveCanBlock
title: IMemInputPin::ReceiveCanBlock (strmif.h)
description: The ReceiveCanBlock method determines whether calls to the IMemInputPin::Receive method might block.
helpviewer_keywords: ["IMemInputPin interface [DirectShow]","ReceiveCanBlock method","IMemInputPin.ReceiveCanBlock","IMemInputPin::ReceiveCanBlock","IMemInputPinReceiveCanBlock","ReceiveCanBlock","ReceiveCanBlock method [DirectShow]","ReceiveCanBlock method [DirectShow]","IMemInputPin interface","dshow.imeminputpin_receivecanblock","strmif/IMemInputPin::ReceiveCanBlock"]
old-location: dshow\imeminputpin_receivecanblock.htm
tech.root: dshow
ms.assetid: cc047cad-e250-41f7-856d-26fc077f87a1
ms.date: 4/26/2023
ms.keywords: IMemInputPin interface [DirectShow],ReceiveCanBlock method, IMemInputPin.ReceiveCanBlock, IMemInputPin::ReceiveCanBlock, IMemInputPinReceiveCanBlock, ReceiveCanBlock, ReceiveCanBlock method [DirectShow], ReceiveCanBlock method [DirectShow],IMemInputPin interface, dshow.imeminputpin_receivecanblock, strmif/IMemInputPin::ReceiveCanBlock
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
 - IMemInputPin::ReceiveCanBlock
 - strmif/IMemInputPin::ReceiveCanBlock
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
 - IMemInputPin.ReceiveCanBlock
---

# IMemInputPin::ReceiveCanBlock


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ReceiveCanBlock</code> method determines whether calls to the <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">IMemInputPin::Receive</a> method might block.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The pin will not block on a call to <b>Receive</b>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The pin might block on a call to <b>Receive</b>.

</td>
</tr>
</table>

## -remarks

If this method returns S_FALSE, calls to the <b>Receive</b> method are guaranteed not to block. Otherwise, they might block. An upstream filter can use this method to determine its threading strategy. If calls to <b>Receive</b> can block, the upstream filter might decide to use a worker thread that buffers data.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin Interface</a>
