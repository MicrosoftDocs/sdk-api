---
UID: NF:strmif.IMemAllocator.GetBuffer
title: IMemAllocator::GetBuffer (strmif.h)
description: The GetBuffer method retrieves a media sample that contains an empty buffer.
helpviewer_keywords: ["GetBuffer","GetBuffer method [DirectShow]","GetBuffer method [DirectShow]","IMemAllocator interface","IMemAllocator interface [DirectShow]","GetBuffer method","IMemAllocator.GetBuffer","IMemAllocator::GetBuffer","IMemAllocatorGetBuffer","dshow.imemallocator_getbuffer","strmif/IMemAllocator::GetBuffer"]
old-location: dshow\imemallocator_getbuffer.htm
tech.root: dshow
ms.assetid: a5d015c8-ef15-4bac-906f-5d064fbff11f
ms.date: 4/26/2023
ms.keywords: GetBuffer, GetBuffer method [DirectShow], GetBuffer method [DirectShow],IMemAllocator interface, IMemAllocator interface [DirectShow],GetBuffer method, IMemAllocator.GetBuffer, IMemAllocator::GetBuffer, IMemAllocatorGetBuffer, dshow.imemallocator_getbuffer, strmif/IMemAllocator::GetBuffer
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
 - IMemAllocator::GetBuffer
 - strmif/IMemAllocator::GetBuffer
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
 - IMemAllocator.GetBuffer
---

# IMemAllocator::GetBuffer


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetBuffer</b> method retrieves a media sample that contains an empty buffer.

## -parameters

### -param ppBuffer [out]

Receives a pointer to the buffer's <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface. The caller must release the interface.

### -param pStartTime [in]

Pointer to the start time of the sample, or <b>NULL</b>.

### -param pEndTime [in]

Pointer to the ending time of the sample, or <b>NULL</b>.

### -param dwFlags [in]

Bitwise combination of zero or more of the following flags:

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AM_GBF_NOTASYNCPOINT</td>
<td>This sample is not a synchronization point. Dynamic format changes are not allowed on this sample. When called on the Overlay Mixer or VMR, this flag implies that the buffer returned will contain an image that is identical to the last image delivered.</td>
</tr>
<tr>
<td>AM_GBF_PREVFRAMESKIPPED</td>
<td>This sample is the first after a discontinuity. (Only the video renderer uses this flag.)</td>
</tr>
<tr>
<td>AM_GBF_NOWAIT</td>
<td>Do not wait for a buffer to become available.</td>
</tr>
<tr>
<td>AM_GBF_NODDSURFACELOCK</td>
<td>Used with the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> to request an unlocked DirectDraw surface. For more information, see <a href="/windows/desktop/DirectShow/working-with-direct3d-render-targets">Working with Direct3D Render Targets</a>.</td>
</tr>
</table>

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
<dt><b>VFW_E_NOT_COMMITTED</b></dt>
</dl>
</td>
<td width="60%">
Allocator is decommitted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Timed out.

</td>
</tr>
</table>

## -remarks

By default, this method blocks until a free sample is available or the allocator is decommitted. If the caller specifies the AM_GBF_NOWAIT flag and no sample is available, the allocator can return immediately with a return value of VFW_E_TIMEOUT. However, allocators are not required to support this flag.

The sample returned in <i>ppBuffer</i> has a valid buffer pointer. The caller is responsible for setting any other properties on the sample, such as the time stamps, the media times, or the sync-point property. (For more information, see <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a>.)

The <i>pStartTime</i> and <i>pEndTime</i> parameters are not applied to the sample. The allocator might use these values to determine which buffer it retrieves. For example, the <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter uses these values to synchronize switching between DirectDraw surfaces. To set the time stamp on the sample, call the <a href="/windows/desktop/api/strmif/nf-strmif-imediasample-settime">IMediaSample::SetTime</a> method.

You must call the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-commit">IMemAllocator::Commit</a> method before calling this method. This method fails after the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-decommit">IMemAllocator::Decommit</a> method is called.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator Interface</a>