---
UID: NN:qnetwork.IAMMediaContent
title: IAMMediaContent (qnetwork.h)
description: The IAMMediaContent interface retrieves metadata from a stream.
helpviewer_keywords: ["IAMMediaContent","IAMMediaContent interface [DirectShow]","IAMMediaContent interface [DirectShow]","described","IAMMediaContentInterface","dshow.iammediacontent","qnetwork/IAMMediaContent"]
old-location: dshow\iammediacontent.htm
tech.root: dshow
ms.assetid: bd9cc96d-9664-41f3-9d4f-e5bdb1cb8d09
ms.date: 4/26/2023
ms.keywords: IAMMediaContent, IAMMediaContent interface [DirectShow], IAMMediaContent interface [DirectShow],described, IAMMediaContentInterface, dshow.iammediacontent, qnetwork/IAMMediaContent
req.header: qnetwork.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaContent
 - qnetwork/IAMMediaContent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMMediaContent
---

# IAMMediaContent interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IAMMediaContent</b> interface retrieves metadata from a stream. Applications can use this interface to retrieve information encoded into a stream, such as the author, title, and copyright. This interface is exposed by the <a href="/windows/desktop/DirectShow/avi-splitter-filter">AVI Splitter</a> filter and the <a href="/windows/desktop/DirectShow/mpeg-1-stream-splitter-filter">MPEG-1 Stream Splitter</a> filter.

Depending on the stream type, a filter might support a subset of the methods on this interface. For example, the AVI Splitter retrieves the copyright, author name, and title from INFO chunks in the AVI file. The remaining methods return <b> E_NOTIMPL</b>.

<div class="alert"><b>Note</b>  Windows Media Player does not use this interface to display metadata.</div>
<div> </div>

## -inheritance

The <b>IAMMediaContent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMMediaContent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To define the interface identifier, include the header file Initguid.h before Qnetwork.h, but after Dshow.h and other header files:

<pre class="syntax" xml:space="preserve"><code>#include &lt;dshow.h&gt;
#include &lt;initguid.h&gt;
#include &lt;qnetwork.h&gt;
</code></pre>
<div class="alert"><b>Note</b>  Make sure that Initguid.h is included only once in your project. Otherwise, you will receive linker errors for duplicate GUID values.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
