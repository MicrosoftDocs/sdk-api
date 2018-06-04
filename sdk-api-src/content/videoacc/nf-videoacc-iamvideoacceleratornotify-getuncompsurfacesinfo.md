---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAMVideoAcceleratorNotify::GetUncompSurfacesInfo


## -description



The <b>GetUncompSurfacesInfo</b> method queries the decoder for the number of uncompressed surfaces to allocate and the pixel format.




## -parameters




### -param pGuid [in]


            Pointer to a GUID that specifies the DXVA profile in use.


### -param pUncompBufferInfo [in, out]


            Pointer to a <a href="https://msdn.microsoft.com/113cc7ba-d05e-48a7-88cb-13645beb16d1">AMVAUncompBufferInfo</a> structure. The decoder fills in this structure with the decoder's requirements for the minimum and maximum number of surfaces and the pixel format.

To get the list of supported pixel formats, the decoder should call <a href="https://msdn.microsoft.com/33f9a4ee-4de9-4853-9581-808d7a07bfc4">IAMVideoAccelerator::GetUncompFormatsSupported</a>.


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



After the video renderer allocates the uncompressed surfaces, it calls the decoder's <a href="https://msdn.microsoft.com/e82c73e6-d32e-4875-9f9d-124a1c6ce504">IAMVideoAcceleratorNotify::SetUncompSurfacesInfo</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/7fd0290c-8fd6-4af6-b510-7a87bc7937de">IAMVideoAcceleratorNotify Interface</a>
 

 

