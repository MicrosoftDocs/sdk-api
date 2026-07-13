---
UID: NF:control.IMediaPosition.put_PrerollTime
title: IMediaPosition::put_PrerollTime (control.h)
description: The put_PrerollTime method sets the amount of data that will be queued before the start position.
helpviewer_keywords: ["IMediaPosition interface [DirectShow]","put_PrerollTime method","IMediaPosition.put_PrerollTime","IMediaPosition::put_PrerollTime","IMediaPositionput_PrerollTime","control/IMediaPosition::put_PrerollTime","dshow.imediaposition_put_prerolltime","put_PrerollTime","put_PrerollTime method [DirectShow]","put_PrerollTime method [DirectShow]","IMediaPosition interface"]
old-location: dshow\imediaposition_put_prerolltime.htm
tech.root: dshow
ms.assetid: a09e6e9f-7e6f-4e53-b805-ee4b9d97f4e7
ms.date: 4/26/2023
ms.keywords: IMediaPosition interface [DirectShow],put_PrerollTime method, IMediaPosition.put_PrerollTime, IMediaPosition::put_PrerollTime, IMediaPositionput_PrerollTime, control/IMediaPosition::put_PrerollTime, dshow.imediaposition_put_prerolltime, put_PrerollTime, put_PrerollTime method [DirectShow], put_PrerollTime method [DirectShow],IMediaPosition interface
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
 - IMediaPosition::put_PrerollTime
 - control/IMediaPosition::put_PrerollTime
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
 - IMediaPosition.put_PrerollTime
---

# IMediaPosition::put_PrerollTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_PrerollTime</b> method sets the amount of data that will be queued before the start position.

## -parameters

### -param llTime [in]

Preroll time, in seconds.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

## -remarks

The <i>preroll</i> is the time prior to the start position at which nonrandom access devices, such as tape players, should start rolling.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition Interface</a>