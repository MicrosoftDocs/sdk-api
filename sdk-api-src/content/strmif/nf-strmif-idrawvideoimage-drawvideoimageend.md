---
UID: NF:strmif.IDrawVideoImage.DrawVideoImageEnd
title: IDrawVideoImage::DrawVideoImageEnd (strmif.h)
description: Note  This interface has been deprecated. New applications should not use it. The DrawVideoImageEnd method turns DirectDraw back on after drawing has been performed.
helpviewer_keywords: ["DrawVideoImageEnd","DrawVideoImageEnd method [DirectShow]","DrawVideoImageEnd method [DirectShow]","IDrawVideoImage interface","IDrawVideoImage interface [DirectShow]","DrawVideoImageEnd method","IDrawVideoImage.DrawVideoImageEnd","IDrawVideoImage::DrawVideoImageEnd","IDrawVideoImageDrawVideoImageEnd","dshow.idrawvideoimage_drawvideoimageend","strmif/IDrawVideoImage::DrawVideoImageEnd"]
old-location: dshow\idrawvideoimage_drawvideoimageend.htm
tech.root: dshow
ms.assetid: 051fa283-849d-494c-bebf-d7adabb807a0
ms.date: 4/26/2023
ms.keywords: DrawVideoImageEnd, DrawVideoImageEnd method [DirectShow], DrawVideoImageEnd method [DirectShow],IDrawVideoImage interface, IDrawVideoImage interface [DirectShow],DrawVideoImageEnd method, IDrawVideoImage.DrawVideoImageEnd, IDrawVideoImage::DrawVideoImageEnd, IDrawVideoImageDrawVideoImageEnd, dshow.idrawvideoimage_drawvideoimageend, strmif/IDrawVideoImage::DrawVideoImageEnd
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDrawVideoImage::DrawVideoImageEnd
 - strmif/IDrawVideoImage::DrawVideoImageEnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDrawVideoImage.DrawVideoImageEnd
---

# IDrawVideoImage::DrawVideoImageEnd


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should not use it.</div>
<div> </div>
The <code>DrawVideoImageEnd</code> method turns DirectDraw back on after drawing has been performed.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-idrawvideoimage">IDrawVideoImage Interface</a>
