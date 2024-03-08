---
UID: NN:strmif.IEnumMediaTypes
title: IEnumMediaTypes (strmif.h)
description: The IEnumMediaTypes interface enumerates a pin's preferred media types.
helpviewer_keywords: ["IEnumMediaTypes","IEnumMediaTypes interface [DirectShow]","IEnumMediaTypes interface [DirectShow]","described","IEnumMediaTypesInterface","dshow.ienummediatypes","strmif/IEnumMediaTypes"]
old-location: dshow\ienummediatypes.htm
tech.root: dshow
ms.assetid: e0021e27-0e08-4d07-9610-08a9b945ae34
ms.date: 4/26/2023
ms.keywords: IEnumMediaTypes, IEnumMediaTypes interface [DirectShow], IEnumMediaTypes interface [DirectShow],described, IEnumMediaTypesInterface, dshow.ienummediatypes, strmif/IEnumMediaTypes
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
 - IEnumMediaTypes
 - strmif/IEnumMediaTypes
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
 - IEnumMediaTypes
---

# IEnumMediaTypes interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IEnumMediaTypes</b> interface enumerates a pin's preferred media types. To obtain this interface, call the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-enummediatypes">IPin::EnumMediaTypes</a> method on the pin. Filters use this interface when they connect to other filters. Applications can also use it to examine a pin's preferred media types. For more information, see <a href="/windows/desktop/DirectShow/enumerating-objects-in-a-filter-graph">Enumerating Objects in a Filter Graph</a>.

This interface implements a standard Component Object Model (COM) collection object. 

If a pin's set of preferred media types changes, some methods on this interface return <b>VFW_E_ENUM_OUT_OF_SYNC</b>. Call the <a href="/windows/desktop/api/strmif/nf-strmif-ienummediatypes-reset">IEnumMediaTypes::Reset</a> method to resynchronize the enumerator.

## -inheritance

The <b>IEnumMediaTypes</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumMediaTypes</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/enumerating-media-types">Enumerating Media Types</a>



<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
