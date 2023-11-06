---
UID: NN:dshowasf.IConfigAsfWriter2
title: IConfigAsfWriter2 (dshowasf.h)
description: The IConfigAsfWriter2 interface extends the IConfigAsfWriter interface, which configures the WM ASF Writer filter.
helpviewer_keywords: ["IConfigAsfWriter2","IConfigAsfWriter2 interface [DirectShow]","IConfigAsfWriter2 interface [DirectShow]","described","IConfigAsfWriter2Interface","dshow.iconfigasfwriter2","dshowasf/IConfigAsfWriter2"]
old-location: dshow\iconfigasfwriter2.htm
tech.root: dshow
ms.assetid: fd931a95-3678-46de-8f17-9e7c27087398
ms.date: 4/26/2023
ms.keywords: IConfigAsfWriter2, IConfigAsfWriter2 interface [DirectShow], IConfigAsfWriter2 interface [DirectShow],described, IConfigAsfWriter2Interface, dshow.iconfigasfwriter2, dshowasf/IConfigAsfWriter2
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigAsfWriter2
 - dshowasf/IConfigAsfWriter2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter2
---

# IConfigAsfWriter2 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IConfigAsfWriter2</code> interface extends the <a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter</a> interface, which configures the <a href="/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter. The <code>IConfigAsfWriter2</code> interface provides additional methods to support the capabilities introduced in the Windows Media Format 9 Series SDK, such as two-pass encoding and support for interlaced output.

## -inheritance

The <b>IConfigAsfWriter2</b> interface inherits from <a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter</a>. <b>IConfigAsfWriter2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter</a>
