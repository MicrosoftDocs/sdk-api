---
UID: NF:d3d11sdklayers.ID3D11TracingDevice.SetShaderTrackingOptionsByType
title: ID3D11TracingDevice::SetShaderTrackingOptionsByType (d3d11sdklayers.h)
description: Sets the reference rasterizer's default race-condition tracking options for the specified resource types.
helpviewer_keywords: ["ID3D11TracingDevice interface [Direct3D 11]","SetShaderTrackingOptionsByType method","ID3D11TracingDevice.SetShaderTrackingOptionsByType","ID3D11TracingDevice::SetShaderTrackingOptionsByType","SetShaderTrackingOptionsByType","SetShaderTrackingOptionsByType method [Direct3D 11]","SetShaderTrackingOptionsByType method [Direct3D 11]","ID3D11TracingDevice interface","d3d11sdklayers/ID3D11TracingDevice::SetShaderTrackingOptionsByType","direct3d11.id3d11tracingdevice_setshadertrackingoptionsbytype"]
old-location: direct3d11\id3d11tracingdevice_setshadertrackingoptionsbytype.htm
tech.root: direct3d11
ms.assetid: ABB83CE4-D612-4797-A9AD-F3C2954E669D
ms.date: 12/05/2018
ms.keywords: ID3D11TracingDevice interface [Direct3D 11],SetShaderTrackingOptionsByType method, ID3D11TracingDevice.SetShaderTrackingOptionsByType, ID3D11TracingDevice::SetShaderTrackingOptionsByType, SetShaderTrackingOptionsByType, SetShaderTrackingOptionsByType method [Direct3D 11], SetShaderTrackingOptionsByType method [Direct3D 11],ID3D11TracingDevice interface, d3d11sdklayers/ID3D11TracingDevice::SetShaderTrackingOptionsByType, direct3d11.id3d11tracingdevice_setshadertrackingoptionsbytype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11TracingDevice::SetShaderTrackingOptionsByType
 - d3d11sdklayers/ID3D11TracingDevice::SetShaderTrackingOptionsByType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler.lib
 - D3DCompiler.dll
api_name:
 - ID3D11TracingDevice.SetShaderTrackingOptionsByType
---

# ID3D11TracingDevice::SetShaderTrackingOptionsByType


## -description

Sets the reference rasterizer's default race-condition tracking options for the specified resource types.

## -parameters

### -param ResourceTypeFlags [in]

A <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type">D3D11_SHADER_TRACKING_RESOURCE_TYPE</a>-typed value that specifies the type of resource to track.

### -param Options [in]

A combination of <a href="/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options">D3D11_SHADER_TRACKING_OPTIONS</a>-typed flags that are combined by using a bitwise <b>OR</b> operation. The resulting value identifies tracking options. If a flag is present, the tracking option that the flag represents is set to "on," otherwise the tracking option is set to "off."

## -returns

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11tracingdevice">ID3D11TracingDevice</a>