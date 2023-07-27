---
UID: NF:mediaobj.IMediaBuffer.GetBufferAndLength
title: IMediaBuffer::GetBufferAndLength (mediaobj.h)
description: The GetBufferAndLength method retrieves the buffer and the size of the valid data in the buffer.
helpviewer_keywords: ["GetBufferAndLength","GetBufferAndLength method [DirectShow]","GetBufferAndLength method [DirectShow]","IMediaBuffer interface","IMediaBuffer interface [DirectShow]","GetBufferAndLength method","IMediaBuffer.GetBufferAndLength","IMediaBuffer::GetBufferAndLength","IMediaBufferGetBufferAndLength","dshow.imediabuffer_getbufferandlength","mediaobj/IMediaBuffer::GetBufferAndLength"]
old-location: dshow\imediabuffer_getbufferandlength.htm
tech.root: dshow
ms.assetid: 255ef101-f004-41c8-afb8-437d21decee5
ms.date: 4/26/2023
ms.keywords: GetBufferAndLength, GetBufferAndLength method [DirectShow], GetBufferAndLength method [DirectShow],IMediaBuffer interface, IMediaBuffer interface [DirectShow],GetBufferAndLength method, IMediaBuffer.GetBufferAndLength, IMediaBuffer::GetBufferAndLength, IMediaBufferGetBufferAndLength, dshow.imediabuffer_getbufferandlength, mediaobj/IMediaBuffer::GetBufferAndLength
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaBuffer::GetBufferAndLength
 - mediaobj/IMediaBuffer::GetBufferAndLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaBuffer.GetBufferAndLength
---

# IMediaBuffer::GetBufferAndLength


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetBufferAndLength</code> method retrieves the buffer and the size of the valid data in the buffer.

## -parameters

### -param ppBuffer [out]

Address of a pointer that receives the buffer array. Can be <b>NULL</b> if <i>pcbLength</i> is not <b>NULL</b>.

### -param pcbLength [out]

Pointer to a variable that receives the size of the valid data, in bytes. Can be <b>NULL</b> if <i>ppBuffer</i> is not <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

Either parameter can be <b>NULL</b>, in which case it does not receive a value. At least one parameter must be non-<b>NULL</b>. If both parameters are <b>NULL</b>, the method returns E_POINTER.

The value returned in the <i>pcbLength</i> parameter is the size of the valid data in the buffer, not the buffer's allocated size. To obtain the buffer's allocated size, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getmaxlength">IMediaBuffer::GetMaxLength</a> method.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer">IMediaBuffer Interface</a>



<a href="/windows/desktop/DirectShow/implementing-imediabuffer">Implementing IMediaBuffer</a>