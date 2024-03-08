---
UID: NN:strmif.IConfigInterleaving
title: IConfigInterleaving (strmif.h)
description: The IConfigInterleaving interface controls how the AVI Mux filter interleaves audio and video samples.
helpviewer_keywords: ["IConfigInterleaving","IConfigInterleaving interface [DirectShow]","IConfigInterleaving interface [DirectShow]","described","IConfigInterleavingInterface","dshow.iconfiginterleaving","strmif/IConfigInterleaving"]
old-location: dshow\iconfiginterleaving.htm
tech.root: dshow
ms.assetid: 68594752-a711-4372-95db-10947bd2ce39
ms.date: 4/26/2023
ms.keywords: IConfigInterleaving, IConfigInterleaving interface [DirectShow], IConfigInterleaving interface [DirectShow],described, IConfigInterleavingInterface, dshow.iconfiginterleaving, strmif/IConfigInterleaving
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
 - IConfigInterleaving
 - strmif/IConfigInterleaving
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
 - IConfigInterleaving
---

# IConfigInterleaving interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IConfigInterleaving</b> interface controls how the <a href="/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter interleaves audio and video samples. Video-authoring applications that handle capturing should use this interface when they need to control how audio samples and video frames will be saved on a disk.

## -inheritance

The <b>IConfigInterleaving</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConfigInterleaving</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
