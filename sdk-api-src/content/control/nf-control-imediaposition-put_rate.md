---
UID: NF:control.IMediaPosition.put_Rate
title: IMediaPosition::put_Rate (control.h)
description: The put_Rate method sets the playback rate.
helpviewer_keywords: ["IMediaPosition interface [DirectShow]","put_Rate method","IMediaPosition.put_Rate","IMediaPosition::put_Rate","IMediaPositionput_Rate","control/IMediaPosition::put_Rate","dshow.imediaposition_put_rate","put_Rate","put_Rate method [DirectShow]","put_Rate method [DirectShow]","IMediaPosition interface"]
old-location: dshow\imediaposition_put_rate.htm
tech.root: dshow
ms.assetid: fba6bb5a-6709-41e6-bf76-182c88ee42e3
ms.date: 4/26/2023
ms.keywords: IMediaPosition interface [DirectShow],put_Rate method, IMediaPosition.put_Rate, IMediaPosition::put_Rate, IMediaPositionput_Rate, control/IMediaPosition::put_Rate, dshow.imediaposition_put_rate, put_Rate, put_Rate method [DirectShow], put_Rate method [DirectShow],IMediaPosition interface
req.header: control.h
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
 - IMediaPosition::put_Rate
 - control/IMediaPosition::put_Rate
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
 - IMediaPosition.put_Rate
---

# IMediaPosition::put_Rate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The put_Rate method sets the playback rate.

## -parameters

### -param dRate [in]

Playback rate. Must not be zero.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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

The playback rate is expressed as a ratio of the normal speed. Thus, 1.0 is normal playback speed, 0.5 is half speed, and 2.0 is twice speed. For audio streams, changing the rate also changes the pitch.

For more information, see the remarks in <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-setrate">IMediaSeeking::SetRate</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition Interface</a>