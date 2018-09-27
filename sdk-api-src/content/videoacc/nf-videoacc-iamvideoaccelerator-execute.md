---
UID: NF:videoacc.IAMVideoAccelerator.Execute
title: IAMVideoAccelerator::Execute
author: windows-sdk-content
description: The Execute method performs a DirectX Video Acceleration (DXVA) decoding operation.
old-location: dshow\iamvideoaccelerator_execute.htm
tech.root: DirectShow
ms.assetid: 12794739-9120-4dc1-b95d-6d390d25726b
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: Execute, Execute method [DirectShow], Execute method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],Execute method, IAMVideoAccelerator.Execute, IAMVideoAccelerator::Execute, IAMVideoAcceleratorExecute, dshow.iamvideoaccelerator_execute, videoacc/IAMVideoAccelerator::Execute
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
 - IAMVideoAccelerator.Execute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoAccelerator::Execute


## -description


The <b>Execute</b> method performs a DirectX Video Acceleration (DXVA) decoding operation.
      


## -parameters




### -param dwFunction [in]

Contains one or more 
            DXVA function numbers. 
          


### -param lpPrivateInputData [in]

Pointer to input data for the decoding operation. The meaning of this data depends on the surface type and function number. For details, refer to the DXVA 1.0 specification.


### -param cbPrivateInputData [in]

Size of the input data, in bytes.


### -param lpPrivateOutputDat

TBD


### -param cbPrivateOutputData [in]

Size of the <i>lpPrivateOutputData</i> buffer, in bytes.
          


### -param dwNumBuffers [in]

Number of elements in the <i>pamvaBufferInfo</i> array.
          


### -param pamvaBufferInfo [in]

Pointer to an array of <a href="https://msdn.microsoft.com/8b018c40-44ae-4033-97b3-efa4b4c1bfb2">AMVABUFFERINFO</a> structures.
          


#### - lpPrivateOutputData [in]

Pointer to a buffer where the video accelerator will write output data.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/78e0a165-5a19-4dca-8d6c-445345772824">IAMVideoAccelerator Interface</a>
 

 

