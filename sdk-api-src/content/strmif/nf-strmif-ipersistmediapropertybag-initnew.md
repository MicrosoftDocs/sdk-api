---
UID: NF:strmif.IPersistMediaPropertyBag.InitNew
title: IPersistMediaPropertyBag::InitNew (strmif.h)
description: The InitNew method initializes the object to receive new properties.
helpviewer_keywords: ["IPersistMediaPropertyBag interface [DirectShow]","InitNew method","IPersistMediaPropertyBag.InitNew","IPersistMediaPropertyBag::InitNew","IPersistMediaPropertyBagInitNew","InitNew","InitNew method [DirectShow]","InitNew method [DirectShow]","IPersistMediaPropertyBag interface","dshow.ipersistmediapropertybag_initnew","strmif/IPersistMediaPropertyBag::InitNew"]
old-location: dshow\ipersistmediapropertybag_initnew.htm
tech.root: dshow
ms.assetid: 46d51c05-b653-4f14-810a-eb49d33da359
ms.date: 4/26/2023
ms.keywords: IPersistMediaPropertyBag interface [DirectShow],InitNew method, IPersistMediaPropertyBag.InitNew, IPersistMediaPropertyBag::InitNew, IPersistMediaPropertyBagInitNew, InitNew, InitNew method [DirectShow], InitNew method [DirectShow],IPersistMediaPropertyBag interface, dshow.ipersistmediapropertybag_initnew, strmif/IPersistMediaPropertyBag::InitNew
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
 - IPersistMediaPropertyBag::InitNew
 - strmif/IPersistMediaPropertyBag::InitNew
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
 - IPersistMediaPropertyBag.InitNew
---

# IPersistMediaPropertyBag::InitNew


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>InitNew</code> method initializes the object to receive new properties.



## -returns

Returns S_OK.

## -remarks

Calling this method on the <a href="/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter clears any properties that were previously set using the <a href="/windows/desktop/api/strmif/nf-strmif-ipersistmediapropertybag-load">Load</a> method.

Calling this method on the <a href="/windows/desktop/DirectShow/avi-splitter-filter">AVI Splitter</a> filter or the <a href="/windows/desktop/DirectShow/wave-parser-filter">WAVE Parser</a> filter has no effect.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipersistmediapropertybag">IPersistMediaPropertyBag Interface</a>
