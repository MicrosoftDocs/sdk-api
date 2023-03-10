---
UID: NF:videoacc.IAMVideoAccelerator.ReleaseBuffer
title: IAMVideoAccelerator::ReleaseBuffer (videoacc.h)
description: The ReleaseBuffer method releases a buffer that was locked by a previous call to IAMVideoAccelerator::GetBuffer.
helpviewer_keywords: ["IAMVideoAccelerator interface [DirectShow]","ReleaseBuffer method","IAMVideoAccelerator.ReleaseBuffer","IAMVideoAccelerator::ReleaseBuffer","IAMVideoAcceleratorReleaseBuffer","ReleaseBuffer","ReleaseBuffer method [DirectShow]","ReleaseBuffer method [DirectShow]","IAMVideoAccelerator interface","dshow.iamvideoaccelerator_releasebuffer","videoacc/IAMVideoAccelerator::ReleaseBuffer"]
old-location: dshow\iamvideoaccelerator_releasebuffer.htm
tech.root: dshow
ms.assetid: 2170cf7e-85c8-4658-84fd-96ebc0d2704f
ms.date: 12/05/2018
ms.keywords: IAMVideoAccelerator interface [DirectShow],ReleaseBuffer method, IAMVideoAccelerator.ReleaseBuffer, IAMVideoAccelerator::ReleaseBuffer, IAMVideoAcceleratorReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [DirectShow], ReleaseBuffer method [DirectShow],IAMVideoAccelerator interface, dshow.iamvideoaccelerator_releasebuffer, videoacc/IAMVideoAccelerator::ReleaseBuffer
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
 - IAMVideoAccelerator::ReleaseBuffer
 - videoacc/IAMVideoAccelerator::ReleaseBuffer
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
 - IAMVideoAccelerator.ReleaseBuffer
---

# IAMVideoAccelerator::ReleaseBuffer


## -description

The <b>ReleaseBuffer</b> method releases a buffer that was locked by a previous call to <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer">IAMVideoAccelerator::GetBuffer</a>.

## -parameters

### -param dwTypeIndex [in]

The surface type of the buffer. Use the same value that was passed to the <i>dwTypeIndex</i> parameter of the <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer">GetBuffer</a> method.

### -param dwBufferIndex [in]

The zero-based index of the buffer. Use the same value that was passed to the <i>dwBufferIndex</i> parameter of the <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer">GetBuffer</a> method.

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

This method unlocks a single buffer. The video decoder calls this method when the buffer is no longer required, after any calls to <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute">IAMVideoAccelerator::Execute</a> have been made using that buffer.

The buffer pointer obtained from <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer">GetBuffer</a> is no longer valid after this call.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>