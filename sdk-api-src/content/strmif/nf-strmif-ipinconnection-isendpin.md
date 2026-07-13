---
UID: NF:strmif.IPinConnection.IsEndPin
title: IPinConnection::IsEndPin (strmif.h)
description: The IsEndPin method indicates whether a reconnection search should end at this pin.
helpviewer_keywords: ["IPinConnection interface [DirectShow]","IsEndPin method","IPinConnection.IsEndPin","IPinConnection::IsEndPin","IPinConnectionIsEndPin","IsEndPin","IsEndPin method [DirectShow]","IsEndPin method [DirectShow]","IPinConnection interface","dshow.ipinconnection_isendpin","strmif/IPinConnection::IsEndPin"]
old-location: dshow\ipinconnection_isendpin.htm
tech.root: dshow
ms.assetid: e078c952-2c3b-48cd-a898-ac2de9fc359a
ms.date: 4/26/2023
ms.keywords: IPinConnection interface [DirectShow],IsEndPin method, IPinConnection.IsEndPin, IPinConnection::IsEndPin, IPinConnectionIsEndPin, IsEndPin, IsEndPin method [DirectShow], IsEndPin method [DirectShow],IPinConnection interface, dshow.ipinconnection_isendpin, strmif/IPinConnection::IsEndPin
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IPinConnection::IsEndPin
 - strmif/IPinConnection::IsEndPin
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
 - IPinConnection.IsEndPin
---

# IPinConnection::IsEndPin


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsEndPin</code> method indicates whether a reconnection search should end at this pin.



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
This pin is not a candidate for reconnection. (The reconnection search should not stop at this pin.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
This pin is a candidate for reconnection. (The reconnection search should stop at this pin.)

</td>
</tr>
</table>

## -remarks

A filter or application can call this method to determine whether the pin is a candidate for dynamic reconnection.

Generally, a sink filter or a filter that splits or merges data should return S_OK. Other filters (for example, simple transform filters) should return S_FALSE.

## -see-also

<a href="/windows/desktop/DirectShow/dynamic-reconnection">Dynamic Reconnection</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipinconnection">IPinConnection Interface</a>
