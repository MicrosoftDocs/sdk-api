---
UID: NF:amstream.IAMMultiMediaStream.AddMediaStream
title: IAMMultiMediaStream::AddMediaStream (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The AddMediaStream method adds a new media stream to the filter graph.
helpviewer_keywords: ["AddMediaStream","AddMediaStream method [DirectShow]","AddMediaStream method [DirectShow]","IAMMultiMediaStream interface","IAMMultiMediaStream interface [DirectShow]","AddMediaStream method","IAMMultiMediaStream.AddMediaStream","IAMMultiMediaStream::AddMediaStream","IAMMultiMediaStreamAddMediaStream","amstream/IAMMultiMediaStream::AddMediaStream","dshow.iammultimediastream_addmediastream"]
old-location: dshow\iammultimediastream_addmediastream.htm
tech.root: dshow
ms.assetid: 3ccfb776-6a4e-48da-857d-6693cf916c40
ms.date: 4/26/2023
ms.keywords: AddMediaStream, AddMediaStream method [DirectShow], AddMediaStream method [DirectShow],IAMMultiMediaStream interface, IAMMultiMediaStream interface [DirectShow],AddMediaStream method, IAMMultiMediaStream.AddMediaStream, IAMMultiMediaStream::AddMediaStream, IAMMultiMediaStreamAddMediaStream, amstream/IAMMultiMediaStream::AddMediaStream, dshow.iammultimediastream_addmediastream
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
 - IAMMultiMediaStream::AddMediaStream
 - amstream/IAMMultiMediaStream::AddMediaStream
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
 - IAMMultiMediaStream.AddMediaStream
---

# IAMMultiMediaStream::AddMediaStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>AddMediaStream</code> method adds a new media stream to the filter graph.

## -parameters

### -param pStreamObject [in]

Pointer to the <b>IUnknown</b> interface of an object that is used to create the new media stream. This parameter can be <b>NULL</b>. See Remarks for more information.

### -param PurposeId [in]

Pointer an <a href="/windows/desktop/DirectShow/mspid">MSPID</a> the specifies the type of media stream to create. This parameter can be <b>NULL</b>.

### -param dwFlags [in]

Bitwise combination of zero or more of the following flags.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AMMSF_ADDDEFAULTRENDERER</td>
<td>Add a default renderer (audio streams only).</td>
</tr>
<tr>
<td>AMMSF_CREATEPEER</td>
<td>Create a new stream based on the object specified in <i>pStreamObject</i>.</td>
</tr>
<tr>
<td>AMMSF_NOSTALL</td>
<td>Create a stream that does not block waiting for <b>Update</b> calls.</td>
</tr>
<tr>
<td>AMMSF_STOPIFNOSAMPLES</td>
<td>Create a stream that stops if there are not samples.</td>
</tr>
</table>

### -param ppNewStream [out]

Address of a variable that receives an <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a> interface pointer.

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
<dt><b>MS_E_PURPOSEID</b></dt>
</dl>
</td>
<td width="60%">
Invalid purpose ID.

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

If <i>pPurposeID</i> is <b>NULL</b>, <i>pStreamObject</i> must specify an <b>IMediaStream</b> object. The object's <b>GetInformation</b> method is used to determine the purpose ID, which is then used to create the new media stream.

If the purpose ID is MSPID_PrimaryAudio and <i>dwFlags</i> includes the AMMSF_ADDDEFAULTRENDERER flag, the method adds the DirectSound Renderer to the filter graph.

If <i>dwFlags</i> includes the AMMSF_CREATEPEER flag, the method uses the object specified by <i>pStreamObject</i> to create a new media stream. In that case, <i>pStreamObject</i> can specify any of the following:

<ul>
<li>An <b>IAMMediaStream</b> pointer.</li>
<li>An <b>IMediaStream</b> pointer.</li>
<li>An <b>IDirectDraw</b> pointer.</li>
</ul>
If neither flag is set, <i>pStreamObject</i> can be any of the following:

<ul>
<li>An <b>IAMMediaStream</b> pointer. The object is added to the multimedia stream.</li>
<li>An <b>IDirectDraw</b> pointer. The DirectDraw object is used to create a default video stream.</li>
<li><b>NULL</b>. A default media stream object is created.</li>
</ul>
If the method succeeds, the caller must release the returned <b>IMediaStream</b> interface.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream Interface</a>