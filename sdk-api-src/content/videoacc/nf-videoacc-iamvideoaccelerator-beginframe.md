---
UID: NF:videoacc.IAMVideoAccelerator.BeginFrame
title: IAMVideoAccelerator::BeginFrame (videoacc.h)
description: The BeginFrame method begins the processing to create a decoded picture.helpviewer_keywords: ["BeginFrame","BeginFrame method [DirectShow]","BeginFrame method [DirectShow]","IAMVideoAccelerator interface","IAMVideoAccelerator interface [DirectShow]","BeginFrame method","IAMVideoAccelerator.BeginFrame","IAMVideoAccelerator::BeginFrame","IAMVideoAcceleratorBeginFrame","dshow.iamvideoaccelerator_beginframe","videoacc/IAMVideoAccelerator::BeginFrame"]
old-location: dshow\iamvideoaccelerator_beginframe.htm
tech.root: DirectShow
ms.assetid: 00077ffe-4acb-4648-9e95-652184e4449b
ms.date: 12/05/2018
ms.keywords: BeginFrame, BeginFrame method [DirectShow], BeginFrame method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],BeginFrame method, IAMVideoAccelerator.BeginFrame, IAMVideoAccelerator::BeginFrame, IAMVideoAcceleratorBeginFrame, dshow.iamvideoaccelerator_beginframe, videoacc/IAMVideoAccelerator::BeginFrame
f1_keywords:
- videoacc/IAMVideoAccelerator.BeginFrame
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMVideoAccelerator.BeginFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoAccelerator::BeginFrame


## -description


The <b>BeginFrame</b> method begins the processing to create a decoded picture.


## -parameters




### -param amvaBeginFrameInfo [in]

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo">AMVABeginFrameInfo</a> structure that contains information needed to begin processing the frame.


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
<dt><b>E_PENDING </b></dt>
</dl>
</td>
<td width="60%">
The uncompressed surface is not yet available for use. For example, it is being read for display.

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

This method might block if no frame buffer is available.

For each call to <b>BeginFrame</b>, the decoder must make a corresponding call to <a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe">IAMVideoAccelerator::EndFrame</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>
 

 

