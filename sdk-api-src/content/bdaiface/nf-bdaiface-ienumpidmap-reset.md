---
UID: NF:bdaiface.IEnumPIDMap.Reset
title: IEnumPIDMap::Reset (bdaiface.h)
description: The Reset method moves the iterator to the beginning of the collection.
helpviewer_keywords: ["IEnumPIDMap interface [DirectShow]","Reset method","IEnumPIDMap.Reset","IEnumPIDMap::Reset","IEnumPIDMapReset","Reset","Reset method [DirectShow]","Reset method [DirectShow]","IEnumPIDMap interface","bdaiface/IEnumPIDMap::Reset","dshow.ienumpidmap_reset"]
old-location: dshow\ienumpidmap_reset.htm
tech.root: dshow
ms.assetid: 4f5cc44e-10c0-441f-b34c-80f94c5f6bca
ms.date: 4/26/2023
ms.keywords: IEnumPIDMap interface [DirectShow],Reset method, IEnumPIDMap.Reset, IEnumPIDMap::Reset, IEnumPIDMapReset, Reset, Reset method [DirectShow], Reset method [DirectShow],IEnumPIDMap interface, bdaiface/IEnumPIDMap::Reset, dshow.ienumpidmap_reset
req.header: bdaiface.h
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
 - IEnumPIDMap::Reset
 - bdaiface/IEnumPIDMap::Reset
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
 - IEnumPIDMap.Reset
---

# IEnumPIDMap::Reset


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Reset</code> method moves the iterator to the beginning of the collection.



## -returns

Returns S_OK if successful. If the method fails,an <b>HRESULT</b> error code is returned.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ienumpidmap">IEnumPIDMap Interface</a>
