---
UID: NE:d3d12.D3D12_SHADER_MIN_PRECISION_SUPPORT
title: D3D12_SHADER_MIN_PRECISION_SUPPORT
author: windows-sdk-content
description: Describes minimum precision support options for shaders in the current graphics driver.
old-location: direct3d12\d3d12_shader_min_precision_support.htm
tech.root: direct3d12
ms.assetid: 04172EA4-B663-49B4-A329-E4B0A8EE4617
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D3D12_SHADER_MIN_PRECISION_SUPPORT, D3D12_SHADER_MIN_PRECISION_SUPPORT enumeration, D3D12_SHADER_MIN_PRECISION_SUPPORT_10_BIT, D3D12_SHADER_MIN_PRECISION_SUPPORT_16_BIT, D3D12_SHADER_MIN_PRECISION_SUPPORT_NONE, d3d12/D3D12_SHADER_MIN_PRECISION_SUPPORT, d3d12/D3D12_SHADER_MIN_PRECISION_SUPPORT_10_BIT, d3d12/D3D12_SHADER_MIN_PRECISION_SUPPORT_16_BIT, d3d12/D3D12_SHADER_MIN_PRECISION_SUPPORT_NONE, direct3d12.d3d12_shader_min_precision_support
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d12.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_SHADER_MIN_PRECISION_SUPPORT
product: Windows
targetos: Windows
req.typenames: D3D12_SHADER_MIN_PRECISION_SUPPORT
req.redist: 
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
 

 

