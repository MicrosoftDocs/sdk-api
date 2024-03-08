---
UID: NN:strmif.IEnumPins
title: IEnumPins (strmif.h)
description: Enumerates pins on a filter.The IBaseFilter::EnumPins method returns this interface.
helpviewer_keywords: ["IEnumPins","IEnumPins interface [DirectShow]","IEnumPins interface [DirectShow]","described","IEnumPinsInterface","dshow.ienumpins","strmif/IEnumPins"]
old-location: dshow\ienumpins.htm
tech.root: dshow
ms.assetid: 839190b4-fd29-4a94-8838-d84adfdd9668
ms.date: 4/26/2023
ms.keywords: IEnumPins, IEnumPins interface [DirectShow], IEnumPins interface [DirectShow],described, IEnumPinsInterface, dshow.ienumpins, strmif/IEnumPins
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
 - IEnumPins
 - strmif/IEnumPins
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
 - IEnumPins
---

# IEnumPins interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Enumerates pins on a filter.

The <a href="/windows/desktop/api/strmif/nf-strmif-ibasefilter-enumpins">IBaseFilter::EnumPins</a> method returns this interface. It is based on the standard Component Object Model (COM) enumerators. 

The filter graph manager uses this interface when it connects filters. Applications can use it to retrieve pins on a filter. For more information, see <a href="/windows/desktop/DirectShow/enumerating-objects-in-a-filter-graph">Enumerating Objects in a Filter Graph</a>.

If the number of pins on the filter changes, some methods on this interface return VFW_E_ENUM_OUT_OF_SYNC. Call the <a href="/windows/desktop/api/strmif/nf-strmif-ienumpins-reset">IEnumPins::Reset</a> method to resynchronize the enumerator.

## -inheritance

The <b>IEnumPins</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumPins</b> also has these types of members:

