---
UID: NN:strmif.IMediaPropertyBag
title: IMediaPropertyBag (strmif.h)
description: The IMediaPropertyBag interface is exposed by the Media Property Bag object.
helpviewer_keywords: ["IMediaPropertyBag","IMediaPropertyBag interface [DirectShow]","IMediaPropertyBag interface [DirectShow]","described","IMediaPropertyBagInterface","dshow.imediapropertybag","strmif/IMediaPropertyBag"]
old-location: dshow\imediapropertybag.htm
tech.root: dshow
ms.assetid: 6f134160-b0aa-44fd-b1b9-938f11349eac
ms.date: 4/26/2023
ms.keywords: IMediaPropertyBag, IMediaPropertyBag interface [DirectShow], IMediaPropertyBag interface [DirectShow],described, IMediaPropertyBagInterface, dshow.imediapropertybag, strmif/IMediaPropertyBag
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
 - IMediaPropertyBag
 - strmif/IMediaPropertyBag
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
 - IMediaPropertyBag
---

# IMediaPropertyBag interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMediaPropertyBag</code> interface is exposed by the <a href="/windows/desktop/DirectShow/media-property-bag">Media Property Bag</a> object. The Media Property Bag is a specialized version of the standard COM property bag, designed for setting and retrieving INFO and DISP chunks in Audio-Video Interleaved (AVI) files.

An INFO chunk contains meta-information about a file, such as author and copyright information. A DISP chunk contains data in Clipboard format. For more information, refer to the resource interchange file format (RIFF) specification.

The media property bag stores the chunks as name/value pairs, as follows:

<ul>
<li>INFO chunks: The name is a string with the form INFO/XXXX, where XXXX is the four-character code that defines the type of meta-information—for example, ICOP for copyright information and IART for author name. The value is any string.</li>
<li>DISP chunks: The name is a string with the form DISP/0000000000, where 0000000000 is the 10-character decimal equivalent of a standard Clipboard format—for example, 0000000008 for CF_DIB. The value is an array of bytes that contains the display data.</li>
</ul>
Use this interface with the <a href="/windows/desktop/api/strmif/nn-strmif-ipersistmediapropertybag">IPersistMediaPropertyBag</a> interface to retrieve INFO and DISP chunks from an AVI file.

## -inheritance

The <b>IMediaPropertyBag</b> interface inherits from <b>IPropertyBag</b>. <b>IMediaPropertyBag</b> also has these types of members:

