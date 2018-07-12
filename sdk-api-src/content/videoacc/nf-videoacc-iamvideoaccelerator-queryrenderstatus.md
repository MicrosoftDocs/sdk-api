---
UID: NF:videoacc.IAMVideoAccelerator.QueryRenderStatus
title: IAMVideoAccelerator::QueryRenderStatus
author: windows-sdk-content
description: The QueryRenderStatus method queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.
old-location: dshow\iamvideoaccelerator_queryrenderstatus.htm
old-project: DirectShow
ms.assetid: 29d77bd5-2823-4e67-a69f-2898ad4c467c
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: AMVA_QUERYRENDERSTATUSF_READ, IAMVideoAccelerator interface [DirectShow],QueryRenderStatus method, IAMVideoAccelerator.QueryRenderStatus, IAMVideoAccelerator::QueryRenderStatus, IAMVideoAcceleratorQueryRenderStatus, QueryRenderStatus, QueryRenderStatus method [DirectShow], QueryRenderStatus method [DirectShow],IAMVideoAccelerator interface, Zero, dshow.iamvideoaccelerator_queryrenderstatus, videoacc/IAMVideoAccelerator::QueryRenderStatus
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
 - IAMVideoAccelerator.QueryRenderStatus
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAMVideoAccelerator::QueryRenderStatus


## -description



        The <b>QueryRenderStatus</b> method queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.
      


## -parameters




### -param dwTypeIndex [in]

Specifies the type of surface to query: 

<ul>
<li>For a compressed surface, specify one of the DXVA surface types defined in dxva.h. </li>
<li>For an uncompressed output surface, set this parameter to 0xFFFFFFFF. </li>
</ul>

### -param dwBufferIndex [in]


            The zero-based index of the surface, within the pool of surfaces that were allocated  for the specified surface type.


### -param dwFlags [in]


            Specifies the type of query to perform.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Zero"></a><a id="zero"></a><a id="ZERO"></a><dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
Test whether the surface is safe to use for writing.

</td>
</tr>
<tr>
<td width="40%"><a id="AMVA_QUERYRENDERSTATUSF_READ"></a><a id="amva_queryrenderstatusf_read"></a><dl>
<dt><b><b>AMVA_QUERYRENDERSTATUSF_READ</b></b></dt>
</dl>
</td>
<td width="60%">
Test whether the surface is safe to use for reading.

</td>
</tr>
</table>
 


## -returns




            Returns an <b>HRESULT</b> value. Possible values include the following:
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation is still in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation is complete.

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




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/78e0a165-5a19-4dca-8d6c-445345772824">IAMVideoAccelerator Interface</a>
 

 

