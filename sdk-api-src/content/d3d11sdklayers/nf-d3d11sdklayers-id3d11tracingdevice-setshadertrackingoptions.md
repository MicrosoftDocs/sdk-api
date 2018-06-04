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

# ID3D11TracingDevice::SetShaderTrackingOptions


## -description


Sets the reference rasterizer's race-condition tracking options for a specific shader.


## -parameters




### -param pShader [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of a shader.


### -param Options [in]

A combination of <a href="https://msdn.microsoft.com/20C152CD-B155-4B46-8F41-EDDEC60494DF">D3D11_SHADER_TRACKING_OPTIONS</a>-typed flags that are combined by using a bitwise <b>OR</b> operation. The resulting value identifies tracking options. If a flag is present, the tracking option that the flag represents is set to "on"; otherwise the tracking option is set to "off."


## -returns



This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



<div class="alert"><b>Note</b>  After a call to <b>SetShaderTrackingOptions</b>, the tracking options that the  <i>Options</i> parameter specifies are set for all calls by the shader that the  <i>pShader</i> parameter specifies, until the next call to <b>SetShaderTrackingOptions</b>. If you set a flag that is specific to unordered access views (UAV) (for example, <a href="d3d11_shader_tracking_options.htm">D3D11_SHADER_TRACKING_OPTION_UAV_SPECIFIC_FLAGS</a>) in the <i>Options</i> parameter for a compute shader, <b>SetShaderTrackingOptions</b> ignores it.</div>
<div> </div>
<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/AE42E2A8-9FEE-4991-B1A0-4C6C04958DE4">ID3D11TracingDevice</a>
 

 

