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
 

 

