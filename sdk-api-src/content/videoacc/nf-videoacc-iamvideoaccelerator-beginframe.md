---
UID: NF:videoacc.IAMVideoAccelerator.BeginFrame
title: IAMVideoAccelerator::BeginFrame
author: windows-sdk-content
description: The BeginFrame method begins the processing to create a decoded picture.
old-location: dshow\iamvideoaccelerator_beginframe.htm
old-project: DirectShow
ms.assetid: 00077ffe-4acb-4648-9e95-652184e4449b
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: BeginFrame, BeginFrame method [DirectShow], BeginFrame method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],BeginFrame method, IAMVideoAccelerator.BeginFrame, IAMVideoAccelerator::BeginFrame, IAMVideoAcceleratorBeginFrame, dshow.iamvideoaccelerator_beginframe, videoacc/IAMVideoAccelerator::BeginFrame
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMVideoAccelerator.BeginFrame
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAMVideoAccelerator::BeginFrame


## -description



        The <b>BeginFrame</b> method begins the processing to create a decoded picture.


## -parameters




### -param amvaBeginFrameInfo






#### - pamvaBeginFrameInfo [in]


            Pointer to an <a href="https://msdn.microsoft.com/49af9094-86d5-4c11-b871-41f9984e0faf">AMVABeginFrameInfo</a> structure that contains information needed to begin processing the frame.


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

For each call to <b>BeginFrame</b>, the decoder must make a corresponding call to <a href="https://msdn.microsoft.com/38944989-2ce2-4275-bae9-faca0d51cca8">IAMVideoAccelerator::EndFrame</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/78e0a165-5a19-4dca-8d6c-445345772824">IAMVideoAccelerator Interface</a>
 

 

