---
UID: NF:videoacc.IAMVideoAccelerator.GetInternalCompBufferInfo
title: IAMVideoAccelerator::GetInternalCompBufferInfo (videoacc.h)
description: The GetInternalCompBufferInfo method gets information about the compressed buffers used for DirectX Video Acceleration (DXVA) decoding.
helpviewer_keywords: ["GetInternalCompBufferInfo","GetInternalCompBufferInfo method [DirectShow]","GetInternalCompBufferInfo method [DirectShow]","IAMVideoAccelerator interface","IAMVideoAccelerator interface [DirectShow]","GetInternalCompBufferInfo method","IAMVideoAccelerator.GetInternalCompBufferInfo","IAMVideoAccelerator::GetInternalCompBufferInfo","IAMVideoAcceleratorGetInternalCompBufferInfo","dshow.iamvideoaccelerator_getinternalcompbufferinfo","videoacc/IAMVideoAccelerator::GetInternalCompBufferInfo"]
old-location: dshow\iamvideoaccelerator_getinternalcompbufferinfo.htm
tech.root: dshow
ms.assetid: b60c6bf7-6cb6-4a82-bec4-7f1662d4ee95
ms.date: 4/26/2023
ms.keywords: GetInternalCompBufferInfo, GetInternalCompBufferInfo method [DirectShow], GetInternalCompBufferInfo method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],GetInternalCompBufferInfo method, IAMVideoAccelerator.GetInternalCompBufferInfo, IAMVideoAccelerator::GetInternalCompBufferInfo, IAMVideoAcceleratorGetInternalCompBufferInfo, dshow.iamvideoaccelerator_getinternalcompbufferinfo, videoacc/IAMVideoAccelerator::GetInternalCompBufferInfo
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
 - IAMVideoAccelerator::GetInternalCompBufferInfo
 - videoacc/IAMVideoAccelerator::GetInternalCompBufferInfo
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
 - IAMVideoAccelerator.GetInternalCompBufferInfo
---

# IAMVideoAccelerator::GetInternalCompBufferInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetInternalCompBufferInfo</b> method gets information about the compressed buffers used for DirectX Video Acceleration (DXVA) decoding.

Call this method after the decoder has connected to the video renderer's input pin. During the pin connection process, use the <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo">IAMVideoAccelerator::GetCompBufferInfo</a> method instead.

## -parameters

### -param pdwNumTypesCompBuffers [in, out]

On input, specifies the number of elements in the <i>pamvaCompBufferInfo</i> array.
            If <i>pamvaCompBufferInfo</i> is <b>NULL</b>, the value of <code>*pdwNumTypesCompBuffers</code> must be zero.

On output, if <i>pamvaCompBufferInfo</i> is <b>NULL</b>, <i>pdwNumTypesCompBuffers</i> receives the size of array to allocate. Otherwise, <i>pdwNumTypesCompBuffers</i> receives the actual number of elements copied to the <i>pamvaCompBufferInfo</i> array.

### -param pamvaCompBufferInfo [out]

Address of an array of <a href="/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo">AMVACompBufferInfo</a> structures, or <b>NULL</b>. If the value is non-<b>NULL</b>, the method copies a list of <b>AMVACompBufferInfo</b> structures to this array. Each structure corresponds to one type of compressed data buffer used by the video accelerator.

Set all of the array elements to zero before calling this method.

Each array index corresponds to one of the DXVA surface types defined in dxva.h. The video accelerator will return a list of up to <b>DXVA_NUM_TYPES_COMP_BUFFERS</b> array entries. For details, refer to the <a href="/windows-hardware/drivers/display/directx-video-acceleration">DXVA 1.0 specification</a>, section 3.4, "Buffer Description List." If a particular buffer type is not used by the DXVA profile in question, the entry at that index contains zeroes for all values.

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

The <a href="/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo">AMVACompBufferInfo</a> structure contains information that is needed for the <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer">IAMVideoAccelerator::GetBuffer</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo">AMVACompBufferInfo Structure</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>