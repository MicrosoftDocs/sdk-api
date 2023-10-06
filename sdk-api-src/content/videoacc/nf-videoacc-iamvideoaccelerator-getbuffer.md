---
UID: NF:videoacc.IAMVideoAccelerator.GetBuffer
title: IAMVideoAccelerator::GetBuffer (videoacc.h)
description: The GetBuffer method gets a pointer to a compressed or uncompressed surface that was allocated for DirectX Video Acceleration (DXVA) decoding.
helpviewer_keywords: ["GetBuffer","GetBuffer method [DirectShow]","GetBuffer method [DirectShow]","IAMVideoAccelerator interface","IAMVideoAccelerator interface [DirectShow]","GetBuffer method","IAMVideoAccelerator.GetBuffer","IAMVideoAccelerator::GetBuffer","IAMVideoAcceleratorGetBuffer","dshow.iamvideoaccelerator_getbuffer","videoacc/IAMVideoAccelerator::GetBuffer"]
old-location: dshow\iamvideoaccelerator_getbuffer.htm
tech.root: dshow
ms.assetid: 3385cad2-8885-4b17-83fa-f40f25b0c433
ms.date: 4/26/2023
ms.keywords: GetBuffer, GetBuffer method [DirectShow], GetBuffer method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],GetBuffer method, IAMVideoAccelerator.GetBuffer, IAMVideoAccelerator::GetBuffer, IAMVideoAcceleratorGetBuffer, dshow.iamvideoaccelerator_getbuffer, videoacc/IAMVideoAccelerator::GetBuffer
req.header: videoacc.h
req.include-header: 
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
 - IAMVideoAccelerator::GetBuffer
 - videoacc/IAMVideoAccelerator::GetBuffer
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
 - IAMVideoAccelerator.GetBuffer
---

# IAMVideoAccelerator::GetBuffer


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetBuffer</b> method gets a pointer to a compressed or uncompressed surface that was allocated for DirectX Video Acceleration (DXVA) decoding.

## -parameters

### -param dwTypeIndex [in]

Specifies the surface type:

<ul>
<li>To get a pointer to  a compressed surface, specify one of the DXVA surface types defined in dxva.h. </li>
<li>To get a pointer to an uncompressed output surface, set this parameter to 0xFFFFFFFF. </li>
</ul>
The value 0xFFFFFFFF is valid only between calls to <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe">IAMVideoAccelerator::BeginFrame</a> and <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe">IAMVideoAccelerator::EndFrame</a>.

### -param dwBufferIndex [in]

The zero-based index of the surface, within the pool of surfaces that were allocated  for the specified surface type.

<ul>
<li>Compressed surfaces: To get the number of allocated surfaces for each surface type, call <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getinternalcompbufferinfo">IAMVideoAccelerator::GetInternalCompBufferInfo</a>.</li>
<li>Uncompressed surfaces: The buffer index must equal the <b>dwDestSurfaceIndex</b> member of the <a href="/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo">AMVABeginFrameInfo</a> structure that was passed to the most recent <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe">IAMVideoAccelerator::BeginFrame</a> call.</li>
</ul>

### -param bReadOnly [in]

Specifies whether the decoder will write to the surface memory. For read-only access, specify <b>TRUE</b>. This might allow faster access to reference frames that are currently in use.

### -param ppBuffer [out]

Receives a pointer to the surface memory. To get the size of the buffer in bytes, call the <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getinternalcompbufferinfo">IAMVideoAccelerator::GetInternalCompBufferInfo</a> method. The size is given in the <b>dwBytesToAllocate</b> member of the <a href="/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo">AMVACompBufferInfo</a> structure that corresponds to <i>dwTypeIndex</i>.

### -param lpStride [out]

Receives the surface stride, in bytes.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. <b>HRESULT</b> can include one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_INVALIDSUBTYPE</b></dt>
</dl>
</td>
<td width="60%">
The decoder did not use a DXVA decoding type when it connected to the video renderer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pins on the decoder and video renderer filters are not connected.

</td>
</tr>
</table>

## -remarks

If the filter's pins are not connected, the method returns <b>VFW_E_NOT_CONNECTED</b>.

This method locks and obtains access to a single buffer. Buffers are identified by type and by index within that type. The <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getinternalcompbufferinfo">IAMVideoAccelerator::GetInternalCompBufferInfo</a> method returns the number of surface types in its <i>pdwNumTypesCompBuffers</i> parameter. This number defines the valid range for <i>dwTypeIndex</i>. For each type, the <b>dwNumCompBuffers</b> member of the <a href="/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo">AMVACompBufferInfo</a> structure gives the number of buffers, which defines the valid range for <i>dwBufferIndex</i>. 
      

To release the buffer, call <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer">IAMVideoAccelerator::ReleaseBuffer</a>.

Until all compressed buffers are released, it is possible that the calling thread will hold the Win16 lock or the DirectDraw lock.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>