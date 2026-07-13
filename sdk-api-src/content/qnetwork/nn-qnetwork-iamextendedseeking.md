---
UID: NN:qnetwork.IAMExtendedSeeking
title: IAMExtendedSeeking (qnetwork.h)
description: The IAMExtendedSeeking interface seeks to a marker in a Windows Media stream or changes the playback rate for a Windows Media file. This interface is implemented by the Windows Media Source filter and the WM ASF Reader filter.
helpviewer_keywords: ["IAMExtendedSeeking","IAMExtendedSeeking interface [DirectShow]","IAMExtendedSeeking interface [DirectShow]","described","IAMExtendedSeekingInterface","dshow.iamextendedseeking","qnetwork/IAMExtendedSeeking"]
old-location: dshow\iamextendedseeking.htm
tech.root: dshow
ms.assetid: 9e0e49af-61ef-408c-8c26-bb29ab26a1f5
ms.date: 4/26/2023
ms.keywords: IAMExtendedSeeking, IAMExtendedSeeking interface [DirectShow], IAMExtendedSeeking interface [DirectShow],described, IAMExtendedSeekingInterface, dshow.iamextendedseeking, qnetwork/IAMExtendedSeeking
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
 - IAMExtendedSeeking
 - qnetwork/IAMExtendedSeeking
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
 - IAMExtendedSeeking
---

# IAMExtendedSeeking interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMExtendedSeeking</code> interface seeks to a marker in a Windows Media stream or changes the playback rate for a Windows Media file. This interface is implemented by the <a href="/windows/desktop/DirectShow/windows-media-source-filter">Windows Media Source</a> filter and the <a href="/windows/desktop/DirectShow/wm-asf-reader-filter">WM ASF Reader</a> filter.

## -inheritance

The <b>IAMExtendedSeeking</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMExtendedSeeking</b> also has these types of members:
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



<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
