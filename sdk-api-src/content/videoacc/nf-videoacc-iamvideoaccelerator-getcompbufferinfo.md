---
UID: NF:videoacc.IAMVideoAccelerator.GetCompBufferInfo
title: IAMVideoAccelerator::GetCompBufferInfo
author: windows-sdk-content
description: The GetCompBufferInfo method gets information about the compressed buffers used for DirectX Video Acceleration (DXVA) decoding.
old-location: dshow\iamvideoaccelerator_getcompbufferinfo.htm
tech.root: DirectShow
ms.assetid: c32fb94d-396f-460a-9e69-1baaf14eff6e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCompBufferInfo, GetCompBufferInfo method [DirectShow], GetCompBufferInfo method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],GetCompBufferInfo method, IAMVideoAccelerator.GetCompBufferInfo, IAMVideoAccelerator::GetCompBufferInfo, IAMVideoAcceleratorGetCompBufferInfo, dshow.iamvideoaccelerator_getcompbufferinfo, videoacc/IAMVideoAccelerator::GetCompBufferInfo
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
 - IAMVideoAccelerator.GetCompBufferInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoAccelerator::GetCompBufferInfo


## -description



The <b>GetCompBufferInfo</b> method gets information about the compressed buffers used for DirectX Video Acceleration (DXVA) decoding. 




## -parameters




### -param pGuid [in]

Pointer to a GUID that specifies the DXVA profile in use.


### -param pamvaUncompDataInfo [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dd373449(v=VS.85).aspx">AMVAUncompDataInfo</a> structure that specifies the size and pixel format of the uncompressed data.


### -param pdwNumTypesCompBuffers [in, out]

On input, specifies the number of elements in the <i>pamvaCompBufferInfo</i> array.
            If <i>pamvaCompBufferInfo</i> is <b>NULL</b>, the value of <code>*pdwNumTypesCompBuffers</code> must be zero.

On output, if <i>pamvaCompBufferInfo</i> is <b>NULL</b>, <i>pdwNumTypesCompBuffers</i> receives the size of array to allocate. Otherwise, <i>pdwNumTypesCompBuffers</i> receives the actual number of elements copied to the <i>pamvaCompBufferInfo</i> array.


### -param pamvaCompBufferInfo [out]

Address of an array of <a href="https://msdn.microsoft.com/en-us/library/Dd373445(v=VS.85).aspx">AMVACompBufferInfo</a> structures, or <b>NULL</b>. If the value is non-<b>NULL</b>, the method copies a list of <b>AMVACompBufferInfo</b> structures to this array. Each structure corresponds to one type of compressed data buffer used by the video accelerator.

Set all of the array elements to zero before calling this method.

Each array index corresponds to one of the DXVA surface types defined in dxva.h. The video accelerator will return a list of up to <b>DXVA_NUM_TYPES_COMP_BUFFERS</b>array entries. For details, refer to the <a href="http://go.microsoft.com/fwlink/p/?linkid=93647">DXVA 1.0 specification</a>, section 3.4, "Buffer Description List." If a particular buffer type is not used by the DXVA profile in question, the entry at that index contains zeroes for all values.


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
</table>
 




## -remarks



The decoder can use this method to get compressed buffer information during the pin connection 
      process. After the pins are connected, the decoder can call <a href="https://msdn.microsoft.com/en-us/library/Dd376005(v=VS.85).aspx">IAMVideoAccelerator::GetInternalCompBufferInfo</a> to get this information.

The <a href="https://msdn.microsoft.com/en-us/library/Dd373445(v=VS.85).aspx">AMVACompBufferInfo</a> structure contains information that is needed for the <a href="https://msdn.microsoft.com/en-us/library/Dd376003(v=VS.85).aspx">IAMVideoAccelerator::GetBuffer</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd373445(v=VS.85).aspx">AMVACompBufferInfo Structure</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd375992(v=VS.85).aspx">IAMVideoAccelerator Interface</a>
 

 

