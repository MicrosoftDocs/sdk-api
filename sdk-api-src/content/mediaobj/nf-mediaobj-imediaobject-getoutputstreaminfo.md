---
UID: NF:mediaobj.IMediaObject.GetOutputStreamInfo
title: IMediaObject::GetOutputStreamInfo (mediaobj.h)
description: The GetOutputStreamInfo method retrieves information about an output stream; for example, whether the stream is discardable, and whether it uses a fixed sample size. This information never changes.
helpviewer_keywords: ["GetOutputStreamInfo","GetOutputStreamInfo method [DirectShow]","GetOutputStreamInfo method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","GetOutputStreamInfo method","IMediaObject.GetOutputStreamInfo","IMediaObject::GetOutputStreamInfo","IMediaObjectGetOutputStreamInfo","dshow.imediaobject_getoutputstreaminfo","mediaobj/IMediaObject::GetOutputStreamInfo"]
old-location: dshow\imediaobject_getoutputstreaminfo.htm
tech.root: dshow
ms.assetid: a21e9943-4aaf-4f0e-a92a-5fcd551fe7e1
ms.date: 4/26/2023
ms.keywords: GetOutputStreamInfo, GetOutputStreamInfo method [DirectShow], GetOutputStreamInfo method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetOutputStreamInfo method, IMediaObject.GetOutputStreamInfo, IMediaObject::GetOutputStreamInfo, IMediaObjectGetOutputStreamInfo, dshow.imediaobject_getoutputstreaminfo, mediaobj/IMediaObject::GetOutputStreamInfo
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
 - IMediaObject::GetOutputStreamInfo
 - mediaobj/IMediaObject::GetOutputStreamInfo
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
 - IMediaObject.GetOutputStreamInfo
---

# IMediaObject::GetOutputStreamInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetOutputStreamInfo</code> method retrieves information about an output stream; for example, whether the stream is discardable, and whether it uses a fixed sample size. This information never changes.

## -parameters

### -param dwOutputStreamIndex

Zero-based index of an output stream on the DMO.

### -param pdwFlags [out]

Pointer to a variable that receives a bitwise combination of zero or more <a href="/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_output_stream_info_flags">DMO_OUTPUT_STREAM_INFO_FLAGS</a> flags.

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

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>