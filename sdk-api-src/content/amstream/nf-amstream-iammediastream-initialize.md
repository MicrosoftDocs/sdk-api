---
UID: NF:amstream.IAMMediaStream.Initialize
title: IAMMediaStream::Initialize (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The Initialize method creates and initializes a new media stream with the specified stream type and purpose ID.
helpviewer_keywords: ["IAMMediaStream interface [DirectShow]","Initialize method","IAMMediaStream.Initialize","IAMMediaStream::Initialize","IAMMediaStreamInitialize","Initialize","Initialize method [DirectShow]","Initialize method [DirectShow]","IAMMediaStream interface","amstream/IAMMediaStream::Initialize","dshow.iammediastream_initialize"]
old-location: dshow\iammediastream_initialize.htm
tech.root: dshow
ms.assetid: b695100b-75a4-4107-828c-e0067290d972
ms.date: 4/26/2023
ms.keywords: IAMMediaStream interface [DirectShow],Initialize method, IAMMediaStream.Initialize, IAMMediaStream::Initialize, IAMMediaStreamInitialize, Initialize, Initialize method [DirectShow], Initialize method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::Initialize, dshow.iammediastream_initialize
req.header: amstream.h
req.include-header: 
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
 - IAMMediaStream::Initialize
 - amstream/IAMMediaStream::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaStream.Initialize
---

# IAMMediaStream::Initialize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>Initialize</code> method creates and initializes a new media stream with the specified stream type and purpose ID.

## -parameters

### -param pSourceObject [in]

Pointer to an <b>IUnknown</b> source object.

### -param dwFlags [in]

Value that modifies the media stream's behavior; it is a combination of one or more of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description</th>
</tr>
<tr>
<td>AMMSF_ADDDEFAULTRENDERER</td>
<td>Add a default renderer.</td>
</tr>
<tr>
<td>AMMSF_CREATEPEER</td>
<td>Create a peer stream based on the same object as a <i>pStreamObject</i>.</td>
</tr>
<tr>
<td>AMMSF_NOSTALL</td>
<td>Run the stream even if <a href="/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update">Update</a> is not called.</td>
</tr>
<tr>
<td>AMMSF_STOPIFNOSAMPLES</td>
<td>Terminates the stream if no samples were created or if the last sample is deleted.</td>
</tr>
</table>

### -param PurposeId [in]

Purpose ID for the new media stream.

### -param StreamType [in]

<a href="/previous-versions/windows/desktop/api/mmstream/ne-mmstream-stream_type">STREAM_TYPE</a> enumeration value that specifies the new media stream's media type.

## -returns

Returns S_OK if successful or E_POINTER if one or more of the required parameters are invalid.

## -remarks

If <i>dwFlags</i> specifies AMMSF_ADDDEFAULTRENDERER, then the default renderer for the given purpose ID is created, if possible. Currently, the only default renderer supported is for audio using DirectSound. In this case, the <i>pStreamObject</i> parameter must be <b>NULL</b> and any calls to the <a href="/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream">IMultiMediaStream::GetMediaStream</a> or <a href="/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams">IMultiMediaStream::EnumMediaStreams</a> method will not recognize the stream.

If <i>dwFlags</i> specifies AMMSF_CREATEPEER, then a media stream is created using <i>pStreamObject</i> and added to the current multimedia stream. The <i>pStreamObject</i> parameter varies depending on the stream type. In general, <i>pStreamObject</i> can point to an <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a> object, in which case a stream with the sample purpose ID and format is created. For <b>IDirectDraw</b> streams, it can also be a pointer to an <b>IDirectDraw</b> interface.

If <i>dwFlags</i> specifies AMMSF_STOPIFNOSAMPLES, then the stream is terminated.

If no flags are set, then <i>pStreamObject</i> can be one of the following.

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>An <a href="/windows/desktop/api/amstream/nn-amstream-iammediastream">IAMMediaStream</a> object</td>
<td>This stream is then added to the streams in the multimedia stream.</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td>In this case a default <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a> object is added to the stream with a default underlying object, if required.</td>
</tr>
<tr>
<td>A pointer to an underlying object</td>
<td>This is used to construct default streams. For video streams, this can be an <b>IDirectDraw</b> pointer.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediastream">IAMMediaStream Interface</a>