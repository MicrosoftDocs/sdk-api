---
UID: NN:strmif.IAMVfwCompressDialogs
title: IAMVfwCompressDialogs (strmif.h)
description: The IAMVfwCompressDialogs interface displays a dialog box provided by a Video for Windows (VFW) codec.
helpviewer_keywords: ["IAMVfwCompressDialogs","IAMVfwCompressDialogs interface [DirectShow]","IAMVfwCompressDialogs interface [DirectShow]","described","IAMVfwCompressDialogsInterface","dshow.iamvfwcompressdialogs","strmif/IAMVfwCompressDialogs"]
old-location: dshow\iamvfwcompressdialogs.htm
tech.root: dshow
ms.assetid: 5cc23d68-e0e6-401a-8d16-63c8c68af241
ms.date: 4/26/2023
ms.keywords: IAMVfwCompressDialogs, IAMVfwCompressDialogs interface [DirectShow], IAMVfwCompressDialogs interface [DirectShow],described, IAMVfwCompressDialogsInterface, dshow.iamvfwcompressdialogs, strmif/IAMVfwCompressDialogs
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
 - IAMVfwCompressDialogs
 - strmif/IAMVfwCompressDialogs
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
 - IAMVfwCompressDialogs
---

# IAMVfwCompressDialogs interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMVfwCompressDialogs</code> interface displays a dialog box provided by a Video for Windows (VFW) codec. The <a href="/windows/desktop/DirectShow/avi-compressor-filter">AVI Compressor</a> filter implements this interface. Applications can use it to display one of the dialog boxes (Configure or About) provided by VFW codecs, and to set and retrieve compressor status.

## -inheritance

The <b>IAMVfwCompressDialogs</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVfwCompressDialogs</b> also has these types of members:

