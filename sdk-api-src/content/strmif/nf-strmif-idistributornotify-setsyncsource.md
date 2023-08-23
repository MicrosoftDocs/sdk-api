---
UID: NF:strmif.IDistributorNotify.SetSyncSource
title: IDistributorNotify::SetSyncSource (strmif.h)
description: The SetSyncSource method is called when a new clock is registered.
helpviewer_keywords: ["IDistributorNotify interface [DirectShow]","SetSyncSource method","IDistributorNotify.SetSyncSource","IDistributorNotify::SetSyncSource","IDistributorNotifySetSyncSource","SetSyncSource","SetSyncSource method [DirectShow]","SetSyncSource method [DirectShow]","IDistributorNotify interface","dshow.idistributornotify_setsyncsource","strmif/IDistributorNotify::SetSyncSource"]
old-location: dshow\idistributornotify_setsyncsource.htm
tech.root: dshow
ms.assetid: 671af56f-a333-441e-9a97-04226b1c3225
ms.date: 4/26/2023
ms.keywords: IDistributorNotify interface [DirectShow],SetSyncSource method, IDistributorNotify.SetSyncSource, IDistributorNotify::SetSyncSource, IDistributorNotifySetSyncSource, SetSyncSource, SetSyncSource method [DirectShow], SetSyncSource method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_setsyncsource, strmif/IDistributorNotify::SetSyncSource
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
 - IDistributorNotify::SetSyncSource
 - strmif/IDistributorNotify::SetSyncSource
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
 - IDistributorNotify.SetSyncSource
---

# IDistributorNotify::SetSyncSource


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetSyncSource</code> method is called when a new clock is registered.

## -parameters

### -param pClock [in]

Pointer to the new clock's <a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock</a> interface.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method is called before the filters are notified. Make sure to use <b>AddRef</b> on the <i>pClock</i> parameter if the plug-in distributor intends to hold it beyond this method call.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idistributornotify">IDistributorNotify Interface</a>