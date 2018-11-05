---
UID: NF:videoacc.IAMVideoAccelerator.DisplayFrame
title: IAMVideoAccelerator::DisplayFrame
author: windows-sdk-content
description: The DisplayFrame method causes the video renderer to display a decoded frame.
old-location: dshow\iamvideoaccelerator_displayframe.htm
tech.root: DirectShow
ms.assetid: 7913401f-881a-4364-8504-b02e85a5e343
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DisplayFrame, DisplayFrame method [DirectShow], DisplayFrame method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],DisplayFrame method, IAMVideoAccelerator.DisplayFrame, IAMVideoAccelerator::DisplayFrame, IAMVideoAcceleratorDisplayFrame, dshow.iamvideoaccelerator_displayframe, videoacc/IAMVideoAccelerator::DisplayFrame
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAMVideoAccelerator.DisplayFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoAccelerator::DisplayFrame


## -description



The <b>DisplayFrame</b> method causes the video renderer to display a decoded frame.




## -parameters




### -param dwFlipToIndex [in]

The surface index of the decoded frame to display.
          


### -param pMediaSample [in]

Pointer to the <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface of a media sample. This sample does not contain a video frame, but is used to specify the time stamp and any sample flags. (For more information about sample flags, see <a href="https://msdn.microsoft.com/4fda7f64-130c-42c8-a671-2e24bdd0b09b">AM_SAMPLE2_PROPERTIES</a>.


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
      

The video decoder calls this method after calling <a href="https://msdn.microsoft.com/38944989-2ce2-4275-bae9-faca0d51cca8">IAMVideoAccelerator::EndFrame</a> for the surface whose index is given in <i>dwFlipToIndex</i>. The index value must match the value of <b>AMVABeginFrameInfo.dwDestSurfaceIndex</b> in a previous call to <a href="https://msdn.microsoft.com/00077ffe-4acb-4648-9e95-652184e4449b">IAMVideoAccelerator::BeginFrame</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/78e0a165-5a19-4dca-8d6c-445345772824">IAMVideoAccelerator Interface</a>
 

 

