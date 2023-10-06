---
UID: NF:strmif.IAMFilterGraphCallback.UnableToRender
title: IAMFilterGraphCallback::UnableToRender (strmif.h)
description: The UnableToRender method is called by the Filter Graph Manager if it cannot find any combination of filters to render the specified pin.
helpviewer_keywords: ["IAMFilterGraphCallback interface [DirectShow]","UnableToRender method","IAMFilterGraphCallback.UnableToRender","IAMFilterGraphCallback::UnableToRender","IAMFilterGraphCallbackUnableToRender","UnableToRender","UnableToRender method [DirectShow]","UnableToRender method [DirectShow]","IAMFilterGraphCallback interface","dshow.iamfiltergraphcallback_unabletorender","strmif/IAMFilterGraphCallback::UnableToRender"]
old-location: dshow\iamfiltergraphcallback_unabletorender.htm
tech.root: dshow
ms.assetid: c7fa0eae-f950-423a-8a89-9a7619b27ce6
ms.date: 4/26/2023
ms.keywords: IAMFilterGraphCallback interface [DirectShow],UnableToRender method, IAMFilterGraphCallback.UnableToRender, IAMFilterGraphCallback::UnableToRender, IAMFilterGraphCallbackUnableToRender, UnableToRender, UnableToRender method [DirectShow], UnableToRender method [DirectShow],IAMFilterGraphCallback interface, dshow.iamfiltergraphcallback_unabletorender, strmif/IAMFilterGraphCallback::UnableToRender
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
 - IAMFilterGraphCallback::UnableToRender
 - strmif/IAMFilterGraphCallback::UnableToRender
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
 - IAMFilterGraphCallback.UnableToRender
---

# IAMFilterGraphCallback::UnableToRender


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>UnableToRender</code> method is called by the Filter Graph Manager if it cannot find any combination of filters to render the specified pin.

## -parameters

### -param pPin

Specifies the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of the pin that could not be rendered.

## -returns

If the return value is S_OK, this Filter Graph Manager attempts to render the pin again. For any other return value, including S_FALSE and other success codes, the Filter Graph Manager continues to build the graph as normal. Typically it will reject the current filter and attempt to use a different filter.

## -remarks

The Filter Graph Manager holds a graph-wide critical section while it calls this method. Therefore, the callback method should avoid calling any methods on the Filter Graph Manager, or any methods on filters that might change the graph state (such as disconnecting pins). Doing so might cause a deadlock or other unexpected behaviors. However, it is safe to query the pin for an interface or check the pin's preferred media type. The main use for this method would be to register a new filter, such as a decoder.

This method uses the thiscall calling convention, rather than __stdcall.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamfiltergraphcallback">IAMFilterGraphCallback Interface</a>



<a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>