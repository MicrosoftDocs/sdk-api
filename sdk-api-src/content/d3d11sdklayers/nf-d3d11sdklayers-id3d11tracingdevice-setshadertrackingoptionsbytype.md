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
 

 

