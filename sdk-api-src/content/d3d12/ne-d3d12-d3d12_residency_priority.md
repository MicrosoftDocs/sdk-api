---
UID: NE:d3d12.D3D12_RESIDENCY_PRIORITY
title: D3D12_RESIDENCY_PRIORITY
author: windows-sdk-content
description: Specifies broad residency priority buckets useful for quickly establishing an application priority scheme.
old-location: direct3d12\d3d12_residency_priority.htm
tech.root: direct3d12
ms.assetid: 40A38135-D974-4A35-8859-6F9FE21FAC8D
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_RESIDENCY_PRIORITY, D3D12_RESIDENCY_PRIORITY enumeration, D3D12_RESIDENCY_PRIORITY_HIGH, D3D12_RESIDENCY_PRIORITY_LOW, D3D12_RESIDENCY_PRIORITY_MAXIMUM, D3D12_RESIDENCY_PRIORITY_MINIMUM, D3D12_RESIDENCY_PRIORITY_NORMAL, d3d12/D3D12_RESIDENCY_PRIORITY, d3d12/D3D12_RESIDENCY_PRIORITY_HIGH, d3d12/D3D12_RESIDENCY_PRIORITY_LOW, d3d12/D3D12_RESIDENCY_PRIORITY_MAXIMUM, d3d12/D3D12_RESIDENCY_PRIORITY_MINIMUM, d3d12/D3D12_RESIDENCY_PRIORITY_NORMAL, direct3d12.d3d12_residency_priority
ms.prod: windows
ms.technology: windows-sdk
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
 - d3d12.h
api_name:
 - D3D12_RESIDENCY_PRIORITY
product: Windows
targetos: Windows
req.typenames: D3D12_RESIDENCY_PRIORITY
req.redist: 
---

# D3D12_RESIDENCY_PRIORITY enumeration


## -description


Specifies broad residency priority buckets useful for quickly establishing an application priority scheme.

Applications can assign priority values other than the five values present in this enumeration.


## -enum-fields




### -field D3D12_RESIDENCY_PRIORITY_MINIMUM

Indicates a minimum priority.


### -field D3D12_RESIDENCY_PRIORITY_LOW

Indicates a low priority.


### -field D3D12_RESIDENCY_PRIORITY_NORMAL

Indicates a normal, medium, priority.


### -field D3D12_RESIDENCY_PRIORITY_HIGH

Indicates a high priority. Applications are discouraged from using priories greater than this. For more information see <a href="https://msdn.microsoft.com/C489AA41-B2FC-418D-8268-9C02E5E10E0D">ID3D12Device1::SetResidencyPriority</a>.


### -field D3D12_RESIDENCY_PRIORITY_MAXIMUM

Indicates a maximum priority. Applications are discouraged from using priorities greater than this; <b>D3D12_RESIDENCY_PRIORITY_MAXIMUM</b> is not guaranteed to be available. For more information see <a href="https://msdn.microsoft.com/C489AA41-B2FC-418D-8268-9C02E5E10E0D">ID3D12Device1::SetResidencyPriority</a>



## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/C489AA41-B2FC-418D-8268-9C02E5E10E0D">SetResidencyPriority</a> method.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

