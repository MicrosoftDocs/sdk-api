---
UID: NF:strmif.IEnumMediaTypes.Next
title: IEnumMediaTypes::Next (strmif.h)
description: The Next method retrieves a specified number of media types.
helpviewer_keywords: ["IEnumMediaTypes interface [DirectShow]","Next method","IEnumMediaTypes.Next","IEnumMediaTypes::Next","IEnumMediaTypesNext","Next","Next method [DirectShow]","Next method [DirectShow]","IEnumMediaTypes interface","dshow.ienummediatypes_next","strmif/IEnumMediaTypes::Next"]
old-location: dshow\ienummediatypes_next.htm
tech.root: dshow
ms.assetid: 7a57fa8e-756b-457c-918a-154fbd085ea3
ms.date: 4/26/2023
ms.keywords: IEnumMediaTypes interface [DirectShow],Next method, IEnumMediaTypes.Next, IEnumMediaTypes::Next, IEnumMediaTypesNext, Next, Next method [DirectShow], Next method [DirectShow],IEnumMediaTypes interface, dshow.ienummediatypes_next, strmif/IEnumMediaTypes::Next
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
 - IEnumMediaTypes::Next
 - strmif/IEnumMediaTypes::Next
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
 - IEnumMediaTypes.Next
---

# IEnumMediaTypes::Next


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Next</b> method retrieves a specified number of media types.

## -parameters

### -param cMediaTypes [in]

The number of media types to retrieve.

### -param ppMediaTypes [out]

The address of an array of <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> pointers. The number of elements in the array is given in the <i>cMediaTypes</i> parameter.

### -param pcFetched [out]

Receives the number of media types returned in <i>ppMediaTypes</i>. This parameter can be <b>NULL</b> if <i>cMediaTypes</i> is 1.

## -returns

Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Did not retrieve as many media types as requested.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
<dt><b>VFW_E_ENUM_OUT_OF_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The pin's state has changed and is now inconsistent with the enumerator.

</td>
</tr>
</table>

## -remarks

The caller passes an array of <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> pointers in <i>ppMediaTypes</i>. The method allocates a number <b>AM_MEDIA_TYPE</b> structures equal to <i>cMediaTypes</i> or to the number of media types that remain in the enumeration, whichever is less. The number of structures allocated is returned in <i>pcFetched</i>. Delete each structure by calling the <a href="/windows/desktop/DirectShow/deletemediatype">DeleteMediaType</a> function.

If the set of media types changes, the enumerator becomes inconsistent with the owning pin. In that case, the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="/windows/desktop/api/strmif/nf-strmif-ienummediatypes-reset">IEnumMediaTypes::Reset</a> method. You can then call the <b>Next</b> method safely.

## -see-also

<a href="/windows/desktop/DirectShow/enumerating-media-types">Enumerating Media Types</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienummediatypes">IEnumMediaTypes Interface</a>