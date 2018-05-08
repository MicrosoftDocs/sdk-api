---
UID: NF:d3d11sdklayers.ID3D11TracingDevice.SetShaderTrackingOptions
title: ID3D11TracingDevice::SetShaderTrackingOptions
author: windows-driver-content
description: Sets the reference rasterizer's race-condition tracking options for a specific shader.
old-location: direct3d11\id3d11tracingdevice_setshadertrackingoptions.htm
old-project: direct3d11
ms.assetid: F62FCA38-AE44-427B-95B4-252AE800845C
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: ID3D11TracingDevice interface [Direct3D 11],SetShaderTrackingOptions method, ID3D11TracingDevice.SetShaderTrackingOptions, ID3D11TracingDevice::SetShaderTrackingOptions, SetShaderTrackingOptions, SetShaderTrackingOptions method [Direct3D 11], SetShaderTrackingOptions method [Direct3D 11],ID3D11TracingDevice interface, d3d11sdklayers/ID3D11TracingDevice::SetShaderTrackingOptions, direct3d11.id3d11tracingdevice_setshadertrackingoptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3DCompiler.lib
-	D3DCompiler.dll
api_name:
-	ID3D11TracingDevice.SetShaderTrackingOptions
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: 
req.irql: 
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
 

 

