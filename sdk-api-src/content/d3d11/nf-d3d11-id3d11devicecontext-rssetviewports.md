---
UID: NF:d3d11.ID3D11DeviceContext.RSSetViewports
title: ID3D11DeviceContext::RSSetViewports
author: windows-sdk-content
description: Bind an array of viewports to the rasterizer stage of the pipeline.
old-location: direct3d11\id3d11devicecontext_rssetviewports.htm
tech.root: direct3d11
ms.assetid: 7326e9a8-edfa-4e5a-a29e-fe7c54a055f5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],RSSetViewports method, ID3D11DeviceContext.RSSetViewports, ID3D11DeviceContext::RSSetViewports, RSSetViewports, RSSetViewports method [Direct3D 11], RSSetViewports method [Direct3D 11],ID3D11DeviceContext interface, cdf57cc3-a89c-db1a-5bd9-f1eec144bfe0, d3d11/ID3D11DeviceContext::RSSetViewports, direct3d11.id3d11devicecontext_rssetviewports
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.RSSetViewports
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::RSSetViewports


## -description


Bind an array of viewports to the rasterizer stage of the pipeline.


## -parameters




### -param NumViewports [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of viewports to bind.


### -param pViewports [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/7ef29e40-4b42-4794-83b6-44581c0d529f">D3D11_VIEWPORT</a>*</b>

An array of <a href="https://msdn.microsoft.com/7ef29e40-4b42-4794-83b6-44581c0d529f">D3D11_VIEWPORT</a> structures to bind to the device. See the structure page for details about how the viewport size is dependent on the device feature level which has changed between Direct3D 11 and Direct3D 10.


## -returns



Returns nothing.




## -remarks



All viewports must be set atomically as one operation. Any viewports not defined by the call are disabled.

Which viewport to use is determined by the <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">SV_ViewportArrayIndex</a> semantic output by a geometry shader; if a geometry shader does not specify the semantic, Direct3D will use the first viewport in the array.

<div class="alert"><b>Note</b>  Even though you specify float values to the members of the <a href="https://msdn.microsoft.com/7ef29e40-4b42-4794-83b6-44581c0d529f">D3D11_VIEWPORT</a> structure for the <i>pViewports</i> array in a call to  <b>ID3D11DeviceContext::RSSetViewports</b> for <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature levels</a> 9_x, <b>RSSetViewports</b> uses DWORDs internally. Because of this behavior, when you use a negative top left corner for the viewport, the call to  <b>RSSetViewports</b> for feature levels 9_x fails. This failure occurs because <b>RSSetViewports</b> for 9_x casts the floating point values into unsigned integers without validation, which results in integer overflow. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

