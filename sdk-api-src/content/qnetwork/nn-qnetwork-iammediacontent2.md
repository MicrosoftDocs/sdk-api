---
UID: NN:qnetwork.IAMMediaContent2
title: IAMMediaContent2 (qnetwork.h)
description: The IAMMediaContent2 interface retrieves custom parameters and playlists from ASX files. This interface is not implemented by any default components in DirectShow.
helpviewer_keywords: ["IAMMediaContent2","IAMMediaContent2 interface [DirectShow]","IAMMediaContent2 interface [DirectShow]","described","IAMMediaContent2Interface","dshow.iammediacontent2","qnetwork/IAMMediaContent2"]
old-location: dshow\iammediacontent2.htm
tech.root: dshow
ms.assetid: cf8381f2-2ef0-4169-8029-bce36bf3d6a9
ms.date: 4/26/2023
ms.keywords: IAMMediaContent2, IAMMediaContent2 interface [DirectShow], IAMMediaContent2 interface [DirectShow],described, IAMMediaContent2Interface, dshow.iammediacontent2, qnetwork/IAMMediaContent2
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
 - IAMMediaContent2
 - qnetwork/IAMMediaContent2
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
 - IAMMediaContent2
---

# IAMMediaContent2 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMMediaContent2</code> interface retrieves custom parameters and playlists from ASX files. This interface is not implemented by any default components in DirectShow.

## -inheritance

The <b>IAMMediaContent2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMMediaContent2</b> also has these types of members:
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
