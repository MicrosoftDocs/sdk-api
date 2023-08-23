---
UID: NN:strmif.IGraphConfigCallback
title: IGraphConfigCallback (strmif.h)
description: The IGraphConfigCallback interface contains the callback method passed to IGraphConfig::Reconfigure. The caller (an application or filter) implements this interface. For more information, see IGraphConfig.
helpviewer_keywords: ["IGraphConfigCallback","IGraphConfigCallback interface [DirectShow]","IGraphConfigCallback interface [DirectShow]","described","IGraphConfigCallbackInterface","dshow.igraphconfigcallback","strmif/IGraphConfigCallback"]
old-location: dshow\igraphconfigcallback.htm
tech.root: dshow
ms.assetid: b7856181-1616-4984-bf5e-402140ab7b4e
ms.date: 4/26/2023
ms.keywords: IGraphConfigCallback, IGraphConfigCallback interface [DirectShow], IGraphConfigCallback interface [DirectShow],described, IGraphConfigCallbackInterface, dshow.igraphconfigcallback, strmif/IGraphConfigCallback
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGraphConfigCallback
 - strmif/IGraphConfigCallback
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
 - IGraphConfigCallback
---

# IGraphConfigCallback interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IGraphConfigCallback</code> interface contains the callback method passed to <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconfigure">IGraphConfig::Reconfigure</a>. The caller (an application or filter) implements this interface. For more information, see <a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig</a>.

## -inheritance

The <b>IGraphConfigCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGraphConfigCallback</b> also has these types of members:

