---
UID: NN:qnetwork.IAMChannelInfo
title: IAMChannelInfo (qnetwork.h)
description: The IAMChannelInfo interface gets and sets channel information for Windows Media Station (.nsc) files.This interface is exposed by the Windows Media Source filter only when the filter is reading Windows Media Station (.nsc) files.
helpviewer_keywords: ["IAMChannelInfo","IAMChannelInfo interface [DirectShow]","IAMChannelInfo interface [DirectShow]","described","IAMChannelInfoInterface","dshow.iamchannelinfo","qnetwork/IAMChannelInfo"]
old-location: dshow\iamchannelinfo.htm
tech.root: dshow
ms.assetid: 779d1c0a-f838-4d02-8254-d66916d3b790
ms.date: 4/26/2023
ms.keywords: IAMChannelInfo, IAMChannelInfo interface [DirectShow], IAMChannelInfo interface [DirectShow],described, IAMChannelInfoInterface, dshow.iamchannelinfo, qnetwork/IAMChannelInfo
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
 - IAMChannelInfo
 - qnetwork/IAMChannelInfo
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
 - IAMChannelInfo
---

# IAMChannelInfo interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IAMChannelInfo</b> interface gets and sets channel information for Windows Media Station (.nsc) files.

This interface is exposed by the <a href="/windows/desktop/DirectShow/windows-media-source-filter">Windows Media Source</a> filter only when the filter is reading Windows Media Station (.nsc) files. The Windows Media Source filter uses .nsc files to get the information it needs to receive multicast content over the Internet. These files contain information such as stream location and rollover URL, as well as descriptive information about the station.

## -inheritance

The <b>IAMChannelInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMChannelInfo</b> also has these types of members:
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
