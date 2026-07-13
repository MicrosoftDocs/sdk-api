---
UID: NN:dshowasf.IConfigAsfWriter
title: IConfigAsfWriter (dshowasf.h)
description: The IConfigAsfWriter interface configures the WM ASF Writer filter.
helpviewer_keywords: ["IConfigAsfWriter","IConfigAsfWriter interface [DirectShow]","IConfigAsfWriter interface [DirectShow]","described","IConfigAsfWriterInterface","dshow.iconfigasfwriter","dshowasf/IConfigAsfWriter"]
old-location: dshow\iconfigasfwriter.htm
tech.root: dshow
ms.assetid: 50fd7825-4844-4a7f-b949-4abfff5ef30f
ms.date: 4/26/2023
ms.keywords: IConfigAsfWriter, IConfigAsfWriter interface [DirectShow], IConfigAsfWriter interface [DirectShow],described, IConfigAsfWriterInterface, dshow.iconfigasfwriter, dshowasf/IConfigAsfWriter
req.header: dshowasf.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigAsfWriter
 - dshowasf/IConfigAsfWriter
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
 - IConfigAsfWriter
---

# IConfigAsfWriter interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IConfigAsfWriter</code> interface configures the <a href="/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter. It provides methods for getting and setting the profiles and indexing mode.

When the WM ASF Writer filter is created, it is configured automatically with a default ASF audio-visual profile based on the incoming streams. A profile describes various attributes of an ASF file such as bit rate, number and type of streams, compression quality, and so on. The filter uses the profile to determine what kind of ASF file to write, how many input pins to create, and what media types to accept. When the WM ASF Writer filter is first created, it is configured automatically with the following default profile: WMProfile_V80_256Video. However, using this profile is not recommended because it does not use the Windows Media Audio and Video 9 Series codecs.

## -inheritance

The <b>IConfigAsfWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConfigAsfWriter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>
