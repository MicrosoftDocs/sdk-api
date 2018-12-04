---
UID: NF:d3d11sdklayers.ID3D11TracingDevice.SetShaderTrackingOptionsByType
title: ID3D11TracingDevice::SetShaderTrackingOptionsByType
author: windows-sdk-content
description: Sets the reference rasterizer's default race-condition tracking options for the specified resource types.
old-location: direct3d11\id3d11tracingdevice_setshadertrackingoptionsbytype.htm
tech.root: direct3d11
ms.assetid: ABB83CE4-D612-4797-A9AD-F3C2954E669D
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ID3D11TracingDevice interface [Direct3D 11],SetShaderTrackingOptionsByType method, ID3D11TracingDevice.SetShaderTrackingOptionsByType, ID3D11TracingDevice::SetShaderTrackingOptionsByType, SetShaderTrackingOptionsByType, SetShaderTrackingOptionsByType method [Direct3D 11], SetShaderTrackingOptionsByType method [Direct3D 11],ID3D11TracingDevice interface, d3d11sdklayers/ID3D11TracingDevice::SetShaderTrackingOptionsByType, direct3d11.id3d11tracingdevice_setshadertrackingoptionsbytype
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D11TracingDevice.SetShaderTrackingOptionsByType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11TracingDevice::SetShaderTrackingOptionsByType


## -description


Sets the reference rasterizer's default race-condition tracking options for the specified resource types.


## -parameters




### -param ResourceTypeFlags [in]

A <a href="https://msdn.microsoft.com/148303AC-E373-4D41-BDF5-0E17B2A3D366">D3D11_SHADER_TRACKING_RESOURCE_TYPE</a>-typed value that specifies the type of resource to track. 


### -param Options [in]

A combination of <a href="https://msdn.microsoft.com/20C152CD-B155-4B46-8F41-EDDEC60494DF">D3D11_SHADER_TRACKING_OPTIONS</a>-typed flags that are combined by using a bitwise <b>OR</b> operation. The resulting value identifies tracking options. If a flag is present, the tracking option that the flag represents is set to "on," otherwise the tracking option is set to "off."


## -returns



This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



This API requires the Windows Software Development Kit (SDK) for Windows 8.




## -see-also




<a href="https://msdn.microsoft.com/AE42E2A8-9FEE-4991-B1A0-4C6C04958DE4">ID3D11TracingDevice</a>
 

 

