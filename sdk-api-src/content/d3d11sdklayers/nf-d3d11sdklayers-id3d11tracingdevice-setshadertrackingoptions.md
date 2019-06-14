---
UID: NF:d3d11sdklayers.ID3D11TracingDevice.SetShaderTrackingOptions
title: ID3D11TracingDevice::SetShaderTrackingOptions (d3d11sdklayers.h)
author: windows-sdk-content
description: Sets the reference rasterizer's race-condition tracking options for a specific shader.
old-location: direct3d11\id3d11tracingdevice_setshadertrackingoptions.htm
tech.root: direct3d11
ms.assetid: F62FCA38-AE44-427B-95B4-252AE800845C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11TracingDevice interface [Direct3D 11],SetShaderTrackingOptions method, ID3D11TracingDevice.SetShaderTrackingOptions, ID3D11TracingDevice::SetShaderTrackingOptions, SetShaderTrackingOptions, SetShaderTrackingOptions method [Direct3D 11], SetShaderTrackingOptions method [Direct3D 11],ID3D11TracingDevice interface, d3d11sdklayers/ID3D11TracingDevice::SetShaderTrackingOptions, direct3d11.id3d11tracingdevice_setshadertrackingoptions
ms.topic: method
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3DCompiler.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler.lib
 - D3DCompiler.dll
api_name:
 - ID3D11TracingDevice.SetShaderTrackingOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11TracingDevice::SetShaderTrackingOptions


## -description


Sets the reference rasterizer's race-condition tracking options for a specific shader.


## -parameters




### -param pShader [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of a shader.


### -param Options [in]

A combination of <a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_option">D3D11_SHADER_TRACKING_OPTIONS</a>-typed flags that are combined by using a bitwise <b>OR</b> operation. The resulting value identifies tracking options. If a flag is present, the tracking option that the flag represents is set to "on"; otherwise the tracking option is set to "off."


## -returns



This method returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.




## -remarks



<div class="alert"><b>Note</b>  After a call to <b>SetShaderTrackingOptions</b>, the tracking options that the  <i>Options</i> parameter specifies are set for all calls by the shader that the  <i>pShader</i> parameter specifies, until the next call to <b>SetShaderTrackingOptions</b>. If you set a flag that is specific to unordered access views (UAV) (for example, <a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_option">D3D11_SHADER_TRACKING_OPTION_UAV_SPECIFIC_FLAGS</a>) in the <i>Options</i> parameter for a compute shader, <b>SetShaderTrackingOptions</b> ignores it.</div>
<div> </div>
<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11tracingdevice">ID3D11TracingDevice</a>
 

 

