---
UID: NN:strmif.IGetCapabilitiesKey
title: IGetCapabilitiesKey (strmif.h)
description: The IGetCapabilitiesKey interface enables an application to retrieve the capabilities of a software or hardware codec from the registry, without creating an instance of the encoder filter.
helpviewer_keywords: ["IGetCapabilitiesKey","IGetCapabilitiesKey interface [DirectShow]","IGetCapabilitiesKey interface [DirectShow]","described","IGetCapabilitiesKeyInterface","dshow.igetcapabilitieskey","strmif/IGetCapabilitiesKey"]
old-location: dshow\igetcapabilitieskey.htm
tech.root: dshow
ms.assetid: 97a9112f-7b7b-4a7e-8f40-bdb148d413c8
ms.date: 4/26/2023
ms.keywords: IGetCapabilitiesKey, IGetCapabilitiesKey interface [DirectShow], IGetCapabilitiesKey interface [DirectShow],described, IGetCapabilitiesKeyInterface, dshow.igetcapabilitieskey, strmif/IGetCapabilitiesKey
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IGetCapabilitiesKey
 - strmif/IGetCapabilitiesKey
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
 - IGetCapabilitiesKey
---

# IGetCapabilitiesKey interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IGetCapabilitiesKey</b> interface enables an application to retrieve the capabilities of a software or hardware codec from the registry, without creating an instance of the encoder filter. The moniker for the codec filter exposes this interface. For more information, see <a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>.

## -inheritance

The <b>IGetCapabilitiesKey</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGetCapabilitiesKey</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
