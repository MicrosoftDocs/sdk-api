---
UID: NF:strmif.IMediaSample2.GetProperties
title: IMediaSample2::GetProperties (strmif.h)
description: The GetProperties method retrieves the properties of a media sample.
helpviewer_keywords: ["GetProperties","GetProperties method [DirectShow]","GetProperties method [DirectShow]","IMediaSample2 interface","IMediaSample2 interface [DirectShow]","GetProperties method","IMediaSample2.GetProperties","IMediaSample2::GetProperties","IMediaSample2GetProperties","dshow.imediasample2_getproperties","strmif/IMediaSample2::GetProperties"]
old-location: dshow\imediasample2_getproperties.htm
tech.root: dshow
ms.assetid: ef20deed-f906-459a-8c2a-f1c929ade9ac
ms.date: 4/26/2023
ms.keywords: GetProperties, GetProperties method [DirectShow], GetProperties method [DirectShow],IMediaSample2 interface, IMediaSample2 interface [DirectShow],GetProperties method, IMediaSample2.GetProperties, IMediaSample2::GetProperties, IMediaSample2GetProperties, dshow.imediasample2_getproperties, strmif/IMediaSample2::GetProperties
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
 - IMediaSample2::GetProperties
 - strmif/IMediaSample2::GetProperties
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
 - IMediaSample2.GetProperties
---

# IMediaSample2::GetProperties


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetProperties</code> method retrieves the properties of a media sample.

## -parameters

### -param cbProperties [in]

Length of property data to retrieve, in bytes.

### -param pbProperties [out]

Pointer to a buffer of size <i>cbProperties</i>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

The retrieved data conforms to the format of the [AM_SAMPLE2_PROPERTIES](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure. You can retrieve a subset of the sample properties by setting <i>cbProperties</i> to a value less than the size of the <b>AM_SAMPLE2_PROPERTIES</b> structure.

For efficiency, the <b>pMediaType</b> member returned in <b>AM_SAMPLE2_PROPERTIES</b> is a pointer to the data stored in the media sample, not a copy of that data. The pointer may become invalid after the sample is passed to another filter, or after the input pin's <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">IMemInputPin::Receive</a> method has completed. Also, do not free the pointer or delete the media type.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample2">IMediaSample2 Interface</a>