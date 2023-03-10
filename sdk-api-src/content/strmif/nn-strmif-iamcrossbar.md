---
UID: NN:strmif.IAMCrossbar
title: IAMCrossbar (strmif.h)
description: The IAMCrossbar interface routes signals from an analog or digital source to a video capture filter.This interface is implemented by the Analog Video Crossbar Filter.
helpviewer_keywords: ["IAMCrossbar","IAMCrossbar interface [DirectShow]","IAMCrossbar interface [DirectShow]","described","IAMCrossbarInterface","dshow.iamcrossbar","strmif/IAMCrossbar"]
old-location: dshow\iamcrossbar.htm
tech.root: dshow
ms.assetid: 9eef4923-62e7-475e-85e6-de8c1eefe483
ms.date: 12/05/2018
ms.keywords: IAMCrossbar, IAMCrossbar interface [DirectShow], IAMCrossbar interface [DirectShow],described, IAMCrossbarInterface, dshow.iamcrossbar, strmif/IAMCrossbar
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
 - IAMCrossbar
 - strmif/IAMCrossbar
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
 - IAMCrossbar
---

# IAMCrossbar interface


## -description

The <code>IAMCrossbar</code> interface routes signals from an analog or digital source to a video capture filter.

This interface is implemented by the <a href="/windows/desktop/DirectShow/analog-video-crossbar-filter">Analog Video Crossbar Filter</a>. The Analog Video Crossbar filter is modeled after a general switching matrix, with <i>n</i> inputs and <i>m</i> outputs. For example, a video card might have two external connectors: a coaxial connector for TV, and an S-video input. These would be represented as input pins on the filter. To select one of the inputs, an application would use the <code>IAMCrossbar</code> interface to "route" an input pin to the filter's output pin, by calling the <a href="/windows/desktop/api/strmif/nf-strmif-iamcrossbar-route">IAMCrossbar::Route</a> method.

## -inheritance

The <b>IAMCrossbar</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMCrossbar</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/working-with-crossbars">Working with Crossbars</a>
