---
UID: NF:videoacc.IAMVideoAccelerator.EndFrame
title: IAMVideoAccelerator::EndFrame (videoacc.h)
description: The EndFrame method ends frame processing.
helpviewer_keywords: ["EndFrame","EndFrame method [DirectShow]","EndFrame method [DirectShow]","IAMVideoAccelerator interface","IAMVideoAccelerator interface [DirectShow]","EndFrame method","IAMVideoAccelerator.EndFrame","IAMVideoAccelerator::EndFrame","IAMVideoAcceleratorEndFrame","dshow.iamvideoaccelerator_endframe","videoacc/IAMVideoAccelerator::EndFrame"]
old-location: dshow\iamvideoaccelerator_endframe.htm
tech.root: dshow
ms.assetid: 38944989-2ce2-4275-bae9-faca0d51cca8
ms.date: 12/05/2018
ms.keywords: EndFrame, EndFrame method [DirectShow], EndFrame method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],EndFrame method, IAMVideoAccelerator.EndFrame, IAMVideoAccelerator::EndFrame, IAMVideoAcceleratorEndFrame, dshow.iamvideoaccelerator_endframe, videoacc/IAMVideoAccelerator::EndFrame
f1_keywords:
- videoacc/IAMVideoAccelerator.EndFrame
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
- IAMVideoAccelerator.EndFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoAccelerator::EndFrame


## -description


The <b>EndFrame</b> method ends frame processing.
      


## -parameters




### -param pEndFrameInfo [in]

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/amva/ns-amva-amvaendframeinfo">AMVAEndFrameInfo</a> structure.
          


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

For more information about this method, see the remarks for  <a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe">IAMVideoAccelerator::BeginFrame</a>.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>
 

 

