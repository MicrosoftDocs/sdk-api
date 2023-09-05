---
UID: NF:mediaobj.IMediaObject.GetOutputType
title: IMediaObject::GetOutputType (mediaobj.h)
description: The GetOutputType method retrieves a preferred media type for a specified output stream.
helpviewer_keywords: ["GetOutputType","GetOutputType method [DirectShow]","GetOutputType method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","GetOutputType method","IMediaObject.GetOutputType","IMediaObject::GetOutputType","IMediaObjectGetOutputType","dshow.imediaobject_getoutputtype","mediaobj/IMediaObject::GetOutputType"]
old-location: dshow\imediaobject_getoutputtype.htm
tech.root: dshow
ms.assetid: a7652472-4091-4ecf-b623-5c6eb01be44a
ms.date: 4/26/2023
ms.keywords: GetOutputType, GetOutputType method [DirectShow], GetOutputType method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetOutputType method, IMediaObject.GetOutputType, IMediaObject::GetOutputType, IMediaObjectGetOutputType, dshow.imediaobject_getoutputtype, mediaobj/IMediaObject::GetOutputType
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
 - IMediaObject::GetOutputType
 - mediaobj/IMediaObject::GetOutputType
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
 - IMediaObject.GetOutputType
---

# IMediaObject::GetOutputType


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetOutputType</code> method retrieves a preferred media type for a specified output stream.

## -parameters

### -param dwOutputStreamIndex

Zero-based index of an output stream on the DMO.

### -param dwTypeIndex

Zero-based index on the set of acceptable media types.

### -param pmt [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure allocated by the caller, or <b>NULL</b>. If this parameter is non-<b>NULL</b>, the method fills the structure with the media type. You can use the value <b>NULL</b> to test whether the type index is in range, by checking the return code.

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
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
Type index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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

## -remarks

Call this method to enumerate an output stream's preferred media types. The DMO assigns each media type an index value, in order of preference. The most preferred type has an index of zero. To enumerate all the types, make successive calls while incrementing the type index, until the method returns DMO_E_NO_MORE_ITEMS. The DMO is not guaranteed to enumerate every media type that it supports.

The format block in the returned type might be <b>NULL</b>. If so, the format type is GUID_NULL. You should check the format type before dereferencing the format block.

If the method succeeds, call <a href="/windows/desktop/api/dmort/nf-dmort-mofreemediatype">MoFreeMediaType</a> to free the format block. (This function is also safe to call when the format block is <b>NULL</b>.)

To set the media type, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype">IMediaObject::SetOutputType</a> method. Setting the media type on one stream can change another stream's preferred types. In fact, a stream might not have a preferred type until the type is set on another stream. For example, a decoder might not have a preferred output type until the input type is set. However, the DMO is not required to update its preferred types dynamically in this fashion. Thus, the types returned by this method are not guaranteed to be valid; they might fail when used in the <b>SetOutputType</b> method.

To test whether a particular media type is acceptable, call <b>SetOutputType</b> with the DMO_SET_TYPEF_TEST_ONLY flag.

To test whether the <i>dwTypeIndex</i> parameter is in range, set <i>pmt</i> to <b>NULL</b>. The method returns S_OK if the index is in range, or DMO_E_NO_MORE_ITEMS if the index is out of range.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>