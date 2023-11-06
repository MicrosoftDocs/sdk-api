---
UID: NN:strmif.IFilterMapper2
title: IFilterMapper2 (strmif.h)
description: Registers and unregisters filters, and locates filters in the registry.
helpviewer_keywords: ["IFilterMapper2","IFilterMapper2 interface [DirectShow]","IFilterMapper2 interface [DirectShow]","described","IFilterMapper2Interface","dshow.ifiltermapper2","strmif/IFilterMapper2"]
old-location: dshow\ifiltermapper2.htm
tech.root: dshow
ms.assetid: 6a3db838-cee3-4a9f-a924-fb55931acc83
ms.date: 4/26/2023
ms.keywords: IFilterMapper2, IFilterMapper2 interface [DirectShow], IFilterMapper2 interface [DirectShow],described, IFilterMapper2Interface, dshow.ifiltermapper2, strmif/IFilterMapper2
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
 - IFilterMapper2
 - strmif/IFilterMapper2
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
 - IFilterMapper2
---

# IFilterMapper2 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Registers and unregisters filters, and locates filters in the registry. The <a href="/windows/desktop/DirectShow/filter-mapper">Filter Mapper</a> helper object implements this interface.

Filters use this interface to register and unregister themselves. When the filter graph manager builds a filter graph, it uses this interface to look up filters and determine their characteristics. Applications can also use this interface to look up filters. For more information, see <a href="/windows/desktop/DirectShow/using-the-filter-mapper">Using the Filter Mapper</a> and <a href="/windows/desktop/DirectShow/how-to-register-directshow-filters">How to Register DirectShow Filters</a>.

## -inheritance

The <b>IFilterMapper2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFilterMapper2</b> also has these types of members:

