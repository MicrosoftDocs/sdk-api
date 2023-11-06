---
UID: NF:strmif.IDistributorNotify.Stop
title: IDistributorNotify::Stop (strmif.h)
description: The Stop method is called when the filter graph is entering a stopped state.
helpviewer_keywords: ["IDistributorNotify interface [DirectShow]","Stop method","IDistributorNotify.Stop","IDistributorNotify::Stop","IDistributorNotifyStop","Stop","Stop method [DirectShow]","Stop method [DirectShow]","IDistributorNotify interface","dshow.idistributornotify_stop","strmif/IDistributorNotify::Stop"]
old-location: dshow\idistributornotify_stop.htm
tech.root: dshow
ms.assetid: 21312954-bc48-402b-a03c-954c01b53231
ms.date: 4/26/2023
ms.keywords: IDistributorNotify interface [DirectShow],Stop method, IDistributorNotify.Stop, IDistributorNotify::Stop, IDistributorNotifyStop, Stop, Stop method [DirectShow], Stop method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_stop, strmif/IDistributorNotify::Stop
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
 - IDistributorNotify::Stop
 - strmif/IDistributorNotify::Stop
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
 - IDistributorNotify.Stop
---

# IDistributorNotify::Stop


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Stop</code> method is called when the filter graph is entering a stopped state.



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
Transition is not complete, but no error has occurred.

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
</table>

## -remarks

This method is called before the filters are notified.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idistributornotify">IDistributorNotify Interface</a>
