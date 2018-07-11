---
UID: NF:videoacc.IAMVideoAccelerator.GetBuffer
title: IAMVideoAccelerator::GetBuffer
author: windows-sdk-content
description: The GetBuffer method gets a pointer to a compressed or uncompressed surface that was allocated for DirectX Video Acceleration (DXVA) decoding.
old-location: dshow\iamvideoaccelerator_getbuffer.htm
old-project: DirectShow
ms.assetid: 3385cad2-8885-4b17-83fa-f40f25b0c433
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetBuffer, GetBuffer method [DirectShow], GetBuffer method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],GetBuffer method, IAMVideoAccelerator.GetBuffer, IAMVideoAccelerator::GetBuffer, IAMVideoAcceleratorGetBuffer, dshow.iamvideoaccelerator_getbuffer, videoacc/IAMVideoAccelerator::GetBuffer
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
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAMVideoAccelerator::GetBuffer


## -description



The <b>GetBuffer</b> method gets a pointer to a compressed or uncompressed surface that was allocated for DirectX Video Acceleration (DXVA) decoding.




## -parameters




### -param dwTypeIndex [in]

Specifies the surface type:

<ul>
<li>To get a pointer to  a compressed surface, specify one of the DXVA surface types defined in dxva.h. </li>
<li>To get a pointer to an uncompressed output surface, set this parameter to 0xFFFFFFFF. </li>
</ul>
The value 0xFFFFFFFF is valid only between calls to <a href="https://msdn.microsoft.com/00077ffe-4acb-4648-9e95-652184e4449b">IAMVideoAccelerator::BeginFrame</a> and <a href="https://msdn.microsoft.com/38944989-2ce2-4275-bae9-faca0d51cca8">IAMVideoAccelerator::EndFrame</a>.


### -param dwBufferIndex [in]

The zero-based index of the surface, within the pool of surfaces that were allocated  for the specified surface type.

<ul>
<li>Compressed surfaces: To get the number of allocated surfaces for each surface type, call <a href="https://msdn.microsoft.com/b60c6bf7-6cb6-4a82-bec4-7f1662d4ee95">IAMVideoAccelerator::GetInternalCompBufferInfo</a>.</li>
<li>Uncompressed surfaces: The buffer index must equal the <b>dwDestSurfaceIndex</b> member of the <a href="https://msdn.microsoft.com/49af9094-86d5-4c11-b871-41f9984e0faf">AMVABeginFrameInfo</a> structure that was passed to the most recent <a href="https://msdn.microsoft.com/00077ffe-4acb-4648-9e95-652184e4449b">IAMVideoAccelerator::BeginFrame</a> call.</li>
</ul>

### -param bReadOnly [in]


            Specifies whether the decoder will write to the surface memory. For read-only access, specify <b>TRUE</b>. This might allow faster access to reference frames that are currently in use.
          


### -param ppBuffer [out]

Receives a pointer to the surface memory. To get the size of the buffer in bytes, call the <a href="https://msdn.microsoft.com/b60c6bf7-6cb6-4a82-bec4-7f1662d4ee95">IAMVideoAccelerator::GetInternalCompBufferInfo</a> method. The size is given in the <b>dwBytesToAllocate</b> member of the <a href="https://msdn.microsoft.com/74ef5dfb-1062-40c6-a2dd-76f46ca8db92">AMVACompBufferInfo</a> structure that corresponds to <i>dwTypeIndex</i>.


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


        This method locks and obtains access to a single buffer. Buffers are identified by type and by index within that type. The <a href="https://msdn.microsoft.com/b60c6bf7-6cb6-4a82-bec4-7f1662d4ee95">IAMVideoAccelerator::GetInternalCompBufferInfo</a> method returns the number of surface types in its <i>pdwNumTypesCompBuffers</i> parameter. This number defines the valid range for <i>dwTypeIndex</i>. For each type, the <b>dwNumCompBuffers</b> member of the <a href="https://msdn.microsoft.com/74ef5dfb-1062-40c6-a2dd-76f46ca8db92">AMVACompBufferInfo</a> structure gives the number of buffers, which defines the valid range for <i>dwBufferIndex</i>. 
      

To release the buffer, call <a href="https://msdn.microsoft.com/2170cf7e-85c8-4658-84fd-96ebc0d2704f">IAMVideoAccelerator::ReleaseBuffer</a>.

Until all compressed buffers are released, it is possible that the calling thread will hold the Win16 lock or the DirectDraw lock.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/78e0a165-5a19-4dca-8d6c-445345772824">IAMVideoAccelerator Interface</a>
 

 

