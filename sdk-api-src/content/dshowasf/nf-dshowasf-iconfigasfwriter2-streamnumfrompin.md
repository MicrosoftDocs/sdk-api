---
UID: NF:dshowasf.IConfigAsfWriter2.StreamNumFromPin
title: IConfigAsfWriter2::StreamNumFromPin (dshowasf.h)
description: The StreamNumFromPin method retrieves the stream number associated with the specified input pin.
helpviewer_keywords: ["IConfigAsfWriter2 interface [DirectShow]","StreamNumFromPin method","IConfigAsfWriter2.StreamNumFromPin","IConfigAsfWriter2::StreamNumFromPin","IConfigAsfWriter2StreamNumFromPin","StreamNumFromPin","StreamNumFromPin method [DirectShow]","StreamNumFromPin method [DirectShow]","IConfigAsfWriter2 interface","dshow.iconfigasfwriter2_streamnumfrompin","dshowasf/IConfigAsfWriter2::StreamNumFromPin"]
old-location: dshow\iconfigasfwriter2_streamnumfrompin.htm
tech.root: dshow
ms.assetid: 374331ec-6665-4ed9-b4ee-6d33b1e2ef2c
ms.date: 4/26/2023
ms.keywords: IConfigAsfWriter2 interface [DirectShow],StreamNumFromPin method, IConfigAsfWriter2.StreamNumFromPin, IConfigAsfWriter2::StreamNumFromPin, IConfigAsfWriter2StreamNumFromPin, StreamNumFromPin, StreamNumFromPin method [DirectShow], StreamNumFromPin method [DirectShow],IConfigAsfWriter2 interface, dshow.iconfigasfwriter2_streamnumfrompin, dshowasf/IConfigAsfWriter2::StreamNumFromPin
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigAsfWriter2::StreamNumFromPin
 - dshowasf/IConfigAsfWriter2::StreamNumFromPin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter2.StreamNumFromPin
---

# IConfigAsfWriter2::StreamNumFromPin


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>StreamNumFromPin</code> method retrieves the stream number associated with the specified input pin.

## -parameters

### -param pPin [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface on the input pin.

### -param pwStreamNum [out]

Receives the stream number.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

You may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running the filter graph. This method is provided because you cannot assume that an ASF stream number is the same as the DirectShow pin number.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2">IConfigAsfWriter2 Interface</a>