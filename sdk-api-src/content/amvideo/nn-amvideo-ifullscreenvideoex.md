---
UID: NN:amvideo.IFullScreenVideoEx
title: IFullScreenVideoEx (amvideo.h)
description: The IFullScreenVideoEx interface is implemented on the Full Screen Renderer filter, which provides full-screen video rendering on older hardware.
helpviewer_keywords: ["IFullScreenVideoEx","IFullScreenVideoEx interface [DirectShow]","IFullScreenVideoEx interface [DirectShow]","described","IFullScreenVideoInterface","amvideo/IFullScreenVideoEx","dshow.ifullscreenvideoex"]
old-location: dshow\ifullscreenvideoex.htm
tech.root: dshow
ms.assetid: 4c9de58f-6ceb-4cf5-b1a5-d3e345e08190
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx, IFullScreenVideoEx interface [DirectShow], IFullScreenVideoEx interface [DirectShow],described, IFullScreenVideoInterface, amvideo/IFullScreenVideoEx, dshow.ifullscreenvideoex
req.header: amvideo.h
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
 - IFullScreenVideoEx
 - amvideo/IFullScreenVideoEx
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
 - IFullScreenVideoEx
---

# IFullScreenVideoEx interface


## -description

The <code>IFullScreenVideoEx</code> interface is implemented on the <a href="/windows/desktop/DirectShow/full-screen-renderer-filter">Full Screen Renderer</a> filter, which provides full-screen video rendering on older hardware. Newer video cards can stretch the video efficiently enough that the Full Screen Renderer is not required. Therefore, both the filter and this interface are now deprecated.

## -inheritance

The <b>IFullScreenVideoEx</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFullScreenVideoEx</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

