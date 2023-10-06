---
UID: NF:strmif.IMediaSample2Config.GetSurface
title: IMediaSample2Config::GetSurface (strmif.h)
description: The GetSurface method returns a pointer to the Direct3D surface managed by this media sample.
helpviewer_keywords: ["GetSurface","GetSurface method [DirectShow]","GetSurface method [DirectShow]","IMediaSample2Config interface","IMediaSample2Config interface [DirectShow]","GetSurface method","IMediaSample2Config.GetSurface","IMediaSample2Config::GetSurface","IMediaSample2ConfigGetSurface","dshow.imediasample2config_getsurface","strmif/IMediaSample2Config::GetSurface"]
old-location: dshow\imediasample2config_getsurface.htm
tech.root: dshow
ms.assetid: c53306ec-cb5c-4f55-afb0-de72386a166d
ms.date: 4/26/2023
ms.keywords: GetSurface, GetSurface method [DirectShow], GetSurface method [DirectShow],IMediaSample2Config interface, IMediaSample2Config interface [DirectShow],GetSurface method, IMediaSample2Config.GetSurface, IMediaSample2Config::GetSurface, IMediaSample2ConfigGetSurface, dshow.imediasample2config_getsurface, strmif/IMediaSample2Config::GetSurface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMediaSample2Config::GetSurface
 - strmif/IMediaSample2Config::GetSurface
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
 - IMediaSample2Config.GetSurface
---

# IMediaSample2Config::GetSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetSurface</code> method returns a pointer to the Direct3D surface managed by this media sample.

## -parameters

### -param ppDirect3DSurface9 [out]

Receives a pointer to the <b>IUnknown</b> interface of the Direct3D surface. The caller must release the interface.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample2config">IMediaSample2Config Interface</a>