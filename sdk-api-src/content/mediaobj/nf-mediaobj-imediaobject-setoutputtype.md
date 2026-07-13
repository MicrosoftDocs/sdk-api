---
UID: NF:mediaobj.IMediaObject.SetOutputType
title: IMediaObject::SetOutputType (mediaobj.h)
description: The SetOutputType method sets the media type on an output stream, or tests whether a media type is acceptable.
helpviewer_keywords: ["IMediaObject interface [DirectShow]","SetOutputType method","IMediaObject.SetOutputType","IMediaObject::SetOutputType","IMediaObjectSetOutputType","SetOutputType","SetOutputType method [DirectShow]","SetOutputType method [DirectShow]","IMediaObject interface","dshow.imediaobject_setoutputtype","mediaobj/IMediaObject::SetOutputType"]
old-location: dshow\imediaobject_setoutputtype.htm
tech.root: dshow
ms.assetid: 1dda3c55-d37b-4e04-9509-0e5197d6b019
ms.date: 4/26/2023
ms.keywords: IMediaObject interface [DirectShow],SetOutputType method, IMediaObject.SetOutputType, IMediaObject::SetOutputType, IMediaObjectSetOutputType, SetOutputType, SetOutputType method [DirectShow], SetOutputType method [DirectShow],IMediaObject interface, dshow.imediaobject_setoutputtype, mediaobj/IMediaObject::SetOutputType
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
 - IMediaObject::SetOutputType
 - mediaobj/IMediaObject::SetOutputType
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
 - IMediaObject.SetOutputType
---

# IMediaObject::SetOutputType


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetOutputType</code> method sets the media type on an output stream, or tests whether a media type is acceptable.

## -parameters

### -param dwOutputStreamIndex

Zero-based index of an output stream on the DMO.

### -param pmt [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure that specifies the media type.

### -param dwFlags

Bitwise combination of zero or more flags from the <a href="/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_set_type_flags">DMO_SET_TYPE_FLAGS</a> enumeration.

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
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_TYPE_NOT_ACCEPTED</b></dt>
</dl>
</td>
<td width="60%">
Media type was not accepted

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Media type is not acceptable

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Media type was set successfully, or is acceptable

</td>
</tr>
</table>

## -remarks

Call this method to test, set, or clear the media type on an output stream:

<ul>
<li>To test the media type without setting it, use the DMO_SET_TYPEF_TEST_ONLY flag. If the media type is not acceptable, the method returns S_FALSE.</li>
<li>To set the media type, set <i>dwFlags</i> to zero. If the media type is not acceptable, the method returns DMO_E_TYPE_NOT_ACCEPTED.</li>
<li>To clear the current media type (if any), use the DMO_SET_TYPEF_CLEAR flag and set <i>pmt</i> to <b>NULL</b>. When the method returns, the stream no longer has a media type. The DMO cannot process samples until the application sets a new media type, unless the stream is optional.</li>
</ul>
The media types that are currently set on other streams can affect whether the media type is acceptable.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>