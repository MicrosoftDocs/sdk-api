---
UID: NF:strmif.IGraphConfigCallback.Reconfigure
title: IGraphConfigCallback::Reconfigure (strmif.h)
description: The Reconfigure method is a callback method passed to IGraphConfig::Reconfigure.
helpviewer_keywords: ["IGraphConfigCallback interface [DirectShow]","Reconfigure method","IGraphConfigCallback.Reconfigure","IGraphConfigCallback::Reconfigure","IGraphConfigCallbackReconfigure","Reconfigure","Reconfigure method [DirectShow]","Reconfigure method [DirectShow]","IGraphConfigCallback interface","dshow.igraphconfigcallback_reconfigure","strmif/IGraphConfigCallback::Reconfigure"]
old-location: dshow\igraphconfigcallback_reconfigure.htm
tech.root: dshow
ms.assetid: b4f44639-b3b0-412e-8b71-e1f994dee0e6
ms.date: 4/26/2023
ms.keywords: IGraphConfigCallback interface [DirectShow],Reconfigure method, IGraphConfigCallback.Reconfigure, IGraphConfigCallback::Reconfigure, IGraphConfigCallbackReconfigure, Reconfigure, Reconfigure method [DirectShow], Reconfigure method [DirectShow],IGraphConfigCallback interface, dshow.igraphconfigcallback_reconfigure, strmif/IGraphConfigCallback::Reconfigure
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
 - IGraphConfigCallback::Reconfigure
 - strmif/IGraphConfigCallback::Reconfigure
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
 - IGraphConfigCallback.Reconfigure
---

# IGraphConfigCallback::Reconfigure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Reconfigure</code> method is a callback method passed to <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconfigure">IGraphConfig::Reconfigure</a>.

## -parameters

### -param pvContext

Value passed in the <b>IGraphConfig::Reconfigure</b> method's <i>pvContext</i> parameter.

### -param dwFlags

Value passed in the <b>IGraphConfig::Reconfigure</b> method's <i>dwFlags</i> parameter.

## -returns

Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

If your application or filter calls <b>IGraphConfig::Reconfigure</b>, you must implement this method and pass it as a callback. The <b>IGraphConfig::Reconfigure</b> method obtains a lock on the filter graph before calling your <code>Reconfigure</code> method. Your method then handles all the other details of dynamic graph building.

If this method succeeds, <b>IGraphConfig::Reconfigure</b> tries to put all the filters in the graph back into a running state. If the method fails, <b>IGraphConfig::Reconfigure</b> returns whatever error code this method returned.

This method allows for specialized graph rebuilding. For a more straightforward approach to dynamic graph building, see <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconnect">IGraphConfig::Reconnect</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphconfigcallback">IGraphConfigCallback Interface</a>