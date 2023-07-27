---
UID: NF:strmif.IMediaSample.SetActualDataLength
title: IMediaSample::SetActualDataLength (strmif.h)
description: The SetActualDataLength method sets the length of the valid data in the buffer.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","SetActualDataLength method","IMediaSample.SetActualDataLength","IMediaSample::SetActualDataLength","IMediaSampleSetActualDataLength","SetActualDataLength","SetActualDataLength method [DirectShow]","SetActualDataLength method [DirectShow]","IMediaSample interface","dshow.imediasample_setactualdatalength","strmif/IMediaSample::SetActualDataLength"]
old-location: dshow\imediasample_setactualdatalength.htm
tech.root: dshow
ms.assetid: db8a768e-7550-4165-8f87-308ec7f2e07f
ms.date: 4/26/2023
ms.keywords: IMediaSample interface [DirectShow],SetActualDataLength method, IMediaSample.SetActualDataLength, IMediaSample::SetActualDataLength, IMediaSampleSetActualDataLength, SetActualDataLength, SetActualDataLength method [DirectShow], SetActualDataLength method [DirectShow],IMediaSample interface, dshow.imediasample_setactualdatalength, strmif/IMediaSample::SetActualDataLength
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
 - IMediaSample::SetActualDataLength
 - strmif/IMediaSample::SetActualDataLength
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
 - IMediaSample.SetActualDataLength
---

# IMediaSample::SetActualDataLength


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetActualDataLength</code> method sets the length of the valid data in the buffer.

## -parameters

### -param __MIDL__IMediaSample0000

Length of the data in the media sample, in bytes.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
<dt><b>VFW_E_BUFFER_OVERFLOW.</b></dt>
</dl>
</td>
<td width="60%">
Length specified in <i>lLen</i> is larger than the buffer size.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>