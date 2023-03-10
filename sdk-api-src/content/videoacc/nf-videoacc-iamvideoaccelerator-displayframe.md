---
UID: NF:videoacc.IAMVideoAccelerator.DisplayFrame
title: IAMVideoAccelerator::DisplayFrame (videoacc.h)
description: The DisplayFrame method causes the video renderer to display a decoded frame.
helpviewer_keywords: ["DisplayFrame","DisplayFrame method [DirectShow]","DisplayFrame method [DirectShow]","IAMVideoAccelerator interface","IAMVideoAccelerator interface [DirectShow]","DisplayFrame method","IAMVideoAccelerator.DisplayFrame","IAMVideoAccelerator::DisplayFrame","IAMVideoAcceleratorDisplayFrame","dshow.iamvideoaccelerator_displayframe","videoacc/IAMVideoAccelerator::DisplayFrame"]
old-location: dshow\iamvideoaccelerator_displayframe.htm
tech.root: dshow
ms.assetid: 7913401f-881a-4364-8504-b02e85a5e343
ms.date: 12/05/2018
ms.keywords: DisplayFrame, DisplayFrame method [DirectShow], DisplayFrame method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],DisplayFrame method, IAMVideoAccelerator.DisplayFrame, IAMVideoAccelerator::DisplayFrame, IAMVideoAcceleratorDisplayFrame, dshow.iamvideoaccelerator_displayframe, videoacc/IAMVideoAccelerator::DisplayFrame
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
 - IAMVideoAccelerator::DisplayFrame
 - videoacc/IAMVideoAccelerator::DisplayFrame
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
 - IAMVideoAccelerator.DisplayFrame
---

# IAMVideoAccelerator::DisplayFrame


## -description

The <b>DisplayFrame</b> method causes the video renderer to display a decoded frame.

## -parameters

### -param dwFlipToIndex [in]

The surface index of the decoded frame to display.

### -param pMediaSample [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface of a media sample. This sample does not contain a video frame, but is used to specify the time stamp and any sample flags. (For more information about sample flags, see <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties">AM_SAMPLE2_PROPERTIES</a>.

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

The method blocks until the video renderer finishes displaying the video frame.
      

The video decoder calls this method after calling <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe">IAMVideoAccelerator::EndFrame</a> for the surface whose index is given in <i>dwFlipToIndex</i>. The index value must match the value of <b>AMVABeginFrameInfo.dwDestSurfaceIndex</b> in a previous call to <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe">IAMVideoAccelerator::BeginFrame</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>