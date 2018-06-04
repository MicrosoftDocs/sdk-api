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

# D3D12_SHADER_MIN_PRECISION_SUPPORT enumeration


## -description



          Describes minimum precision support options for shaders in the current graphics driver.

        


## -enum-fields




### -field D3D12_SHADER_MIN_PRECISION_SUPPORT_NONE

The driver supports only full 32-bit precision for all shader stages.


### -field D3D12_SHADER_MIN_PRECISION_SUPPORT_10_BIT

The driver supports 10-bit precision.


### -field D3D12_SHADER_MIN_PRECISION_SUPPORT_16_BIT

The driver supports 16-bit precision.


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
      


        The returned info just indicates that the graphics hardware can perform HLSL operations at a lower precision than the standard 32-bit float precision, but doesn’t guarantee that the graphics hardware will actually run at a lower precision.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

