---
UID: NF:strmif.IMediaFilter.GetSyncSource
title: IMediaFilter::GetSyncSource (strmif.h)
description: The GetSyncSource method retrieves the current reference clock.
helpviewer_keywords: ["GetSyncSource","GetSyncSource method [DirectShow]","GetSyncSource method [DirectShow]","IMediaFilter interface","IMediaFilter interface [DirectShow]","GetSyncSource method","IMediaFilter.GetSyncSource","IMediaFilter::GetSyncSource","IMediaFilterGetSyncSource","dshow.imediafilter_getsyncsource","strmif/IMediaFilter::GetSyncSource"]
old-location: dshow\imediafilter_getsyncsource.htm
tech.root: dshow
ms.assetid: 5f5eb31c-3a12-45f4-9c95-caafc0267481
ms.date: 4/26/2023
ms.keywords: GetSyncSource, GetSyncSource method [DirectShow], GetSyncSource method [DirectShow],IMediaFilter interface, IMediaFilter interface [DirectShow],GetSyncSource method, IMediaFilter.GetSyncSource, IMediaFilter::GetSyncSource, IMediaFilterGetSyncSource, dshow.imediafilter_getsyncsource, strmif/IMediaFilter::GetSyncSource
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
 - IMediaFilter::GetSyncSource
 - strmif/IMediaFilter::GetSyncSource
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
 - IMediaFilter.GetSyncSource
---

# IMediaFilter::GetSyncSource


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetSyncSource</code> method retrieves the current reference clock.

## -parameters

### -param pClock [out]

Receives a pointer to the clock's <a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock</a> interface. The caller must release the interface.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
</table>

## -remarks

This method returns the same reference clock as the last call to <a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-setsyncsource">IMediaFilter::SetSyncSource</a>. If there is no reference clock, <i>pClock</i> receives the value <b>NULL</b>. When the method returns, if <i>*pClock</i> is non-<b>NULL</b>, the <b>IReferenceClock</b> interface has an outstanding reference count. Be sure to release it when you are done.

You can also call this method on the Filter Graph Manager to determine the current reference clock.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter Interface</a>