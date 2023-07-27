---
UID: NF:videoacc.IAMVideoAccelerator.Execute
title: IAMVideoAccelerator::Execute (videoacc.h)
description: The Execute method performs a DirectX Video Acceleration (DXVA) decoding operation.
helpviewer_keywords: ["Execute","Execute method [DirectShow]","Execute method [DirectShow]","IAMVideoAccelerator interface","IAMVideoAccelerator interface [DirectShow]","Execute method","IAMVideoAccelerator.Execute","IAMVideoAccelerator::Execute","IAMVideoAcceleratorExecute","dshow.iamvideoaccelerator_execute","videoacc/IAMVideoAccelerator::Execute"]
old-location: dshow\iamvideoaccelerator_execute.htm
tech.root: dshow
ms.assetid: 12794739-9120-4dc1-b95d-6d390d25726b
ms.date: 4/26/2023
ms.keywords: Execute, Execute method [DirectShow], Execute method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],Execute method, IAMVideoAccelerator.Execute, IAMVideoAccelerator::Execute, IAMVideoAcceleratorExecute, dshow.iamvideoaccelerator_execute, videoacc/IAMVideoAccelerator::Execute
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
 - IAMVideoAccelerator::Execute
 - videoacc/IAMVideoAccelerator::Execute
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
 - IAMVideoAccelerator.Execute
---

# IAMVideoAccelerator::Execute


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Execute</b> method performs a DirectX Video Acceleration (DXVA) decoding operation.

## -parameters

### -param dwFunction [in]

Contains one or more 
            DXVA function numbers.

### -param lpPrivateInputData [in]

Pointer to input data for the decoding operation. The meaning of this data depends on the surface type and function number. For details, refer to the DXVA 1.0 specification.

### -param cbPrivateInputData [in]

Size of the input data, in bytes.

### -param lpPrivateOutputDat [in]

Pointer to a buffer where the video accelerator will write output data.

### -param cbPrivateOutputData [in]

Size of the <i>lpPrivateOutputData</i> buffer, in bytes.

### -param dwNumBuffers [in]

Number of elements in the <i>pamvaBufferInfo</i> array.

### -param pamvaBufferInfo [in]

Pointer to an array of <a href="/previous-versions/windows/desktop/api/amva/ns-amva-amvabufferinfo">AMVABUFFERINFO</a> structures.

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

The associated buffer list is passed along with a function number (defaulting to zero) and any necessary private data describing the decompression operation. For example, decompressed reference frame information is passed in the buffer list. The buffer list order is important and is defined by the particular decompression operation being performed.
      

Private data can be passed to and from a driver.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>