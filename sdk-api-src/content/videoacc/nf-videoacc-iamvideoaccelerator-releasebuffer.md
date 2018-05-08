---
UID: NF:videoacc.IAMVideoAccelerator.ReleaseBuffer
title: IAMVideoAccelerator::ReleaseBuffer
author: windows-driver-content
description: The ReleaseBuffer method releases a buffer that was locked by a previous call to IAMVideoAccelerator::GetBuffer.
old-location: dshow\iamvideoaccelerator_releasebuffer.htm
old-project: DirectShow
ms.assetid: 2170cf7e-85c8-4658-84fd-96ebc0d2704f
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMVideoAccelerator interface [DirectShow],ReleaseBuffer method, IAMVideoAccelerator.ReleaseBuffer, IAMVideoAccelerator::ReleaseBuffer, IAMVideoAcceleratorReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [DirectShow], ReleaseBuffer method [DirectShow],IAMVideoAccelerator interface, dshow.iamvideoaccelerator_releasebuffer, videoacc/IAMVideoAccelerator::ReleaseBuffer
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
-	IAMVideoAccelerator.ReleaseBuffer
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAMVideoAccelerator::ReleaseBuffer


## -description



The <b>ReleaseBuffer</b> method releases a buffer that was locked by a previous call to <a href="https://msdn.microsoft.com/3385cad2-8885-4b17-83fa-f40f25b0c433">IAMVideoAccelerator::GetBuffer</a>.




## -parameters




### -param dwTypeIndex [in]


            The surface type of the buffer. Use the same value that was passed to the <i>dwTypeIndex</i> parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> method.


### -param dwBufferIndex [in]

The zero-based index of the buffer. Use the same value that was passed to the <i>dwBufferIndex</i> parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> method.
          


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

This method unlocks a single buffer. The video decoder calls this method when the buffer is no longer required, after any calls to <a href="https://msdn.microsoft.com/12794739-9120-4dc1-b95d-6d390d25726b">IAMVideoAccelerator::Execute</a> have been made using that buffer.

The buffer pointer obtained from <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> is no longer valid after this call.
      




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/78e0a165-5a19-4dca-8d6c-445345772824">IAMVideoAccelerator Interface</a>
 

 

