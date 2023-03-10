---
UID: NF:mixerocx.IMixerOCX.OnDraw
title: IMixerOCX::OnDraw (mixerocx.h)
description: The OnDraw method instructs the Overlay Mixer to draw the video rectangle.
helpviewer_keywords: ["IMixerOCX interface [DirectShow]","OnDraw method","IMixerOCX.OnDraw","IMixerOCX::OnDraw","IMixerOCXOnDraw","OnDraw","OnDraw method [DirectShow]","OnDraw method [DirectShow]","IMixerOCX interface","dshow.imixerocx_ondraw","mixerocx/IMixerOCX::OnDraw"]
old-location: dshow\imixerocx_ondraw.htm
tech.root: dshow
ms.assetid: 69b8752b-9f97-422e-8a9a-f49c7a472cb6
ms.date: 12/05/2018
ms.keywords: IMixerOCX interface [DirectShow],OnDraw method, IMixerOCX.OnDraw, IMixerOCX::OnDraw, IMixerOCXOnDraw, OnDraw, OnDraw method [DirectShow], OnDraw method [DirectShow],IMixerOCX interface, dshow.imixerocx_ondraw, mixerocx/IMixerOCX::OnDraw
req.header: mixerocx.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMixerOCX::OnDraw
 - mixerocx/IMixerOCX::OnDraw
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
 - IMixerOCX.OnDraw
---

# IMixerOCX::OnDraw


## -description

The <code>OnDraw</code> method instructs the Overlay Mixer to draw the video rectangle.

## -parameters

### -param hdcDraw [in]

Specifies the device context associated with the parent window.

### -param prcDraw [in]

Specifies the rectangle coordinates of the video rectangle.

## -returns

If the method succeeds, it returns S_OK.

## -remarks

The HDC provided here should not be cached.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>