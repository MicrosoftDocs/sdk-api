---
UID: NF:strmif.IFileSinkFilter2.SetMode
title: IFileSinkFilter2::SetMode (strmif.h)
description: The SetMode method determines whether the file writer destroys the file when it creates the new one.
helpviewer_keywords: ["IFileSinkFilter2 interface [DirectShow]","SetMode method","IFileSinkFilter2.SetMode","IFileSinkFilter2::SetMode","IFileSinkFilter2SetMode","SetMode","SetMode method [DirectShow]","SetMode method [DirectShow]","IFileSinkFilter2 interface","dshow.ifilesinkfilter2_setmode","strmif/IFileSinkFilter2::SetMode"]
old-location: dshow\ifilesinkfilter2_setmode.htm
tech.root: dshow
ms.assetid: a32ae597-1468-4ac8-ae7b-8831d2a9ad6e
ms.date: 4/26/2023
ms.keywords: IFileSinkFilter2 interface [DirectShow],SetMode method, IFileSinkFilter2.SetMode, IFileSinkFilter2::SetMode, IFileSinkFilter2SetMode, SetMode, SetMode method [DirectShow], SetMode method [DirectShow],IFileSinkFilter2 interface, dshow.ifilesinkfilter2_setmode, strmif/IFileSinkFilter2::SetMode
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
 - IFileSinkFilter2::SetMode
 - strmif/IFileSinkFilter2::SetMode
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
 - IFileSinkFilter2.SetMode
---

# IFileSinkFilter2::SetMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetMode</code> method determines whether the file writer destroys the file when it creates the new one.

## -parameters

### -param dwFlags [in]

Currently, the only defined flag is AM_FILE_OVERWRITE, which indicates that the file writer should destroy the file. Specify zero for <i>dwFlags</i> to leave the file alone.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter2">IFileSinkFilter2 Interface</a>