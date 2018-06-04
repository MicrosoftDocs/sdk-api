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

# D3D12_ROOT_PARAMETER_TYPE enumeration


## -description



          Specifies the type of root signature slot.
        


## -enum-fields




### -field D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE


            The slot is for a descriptor table.
          


### -field D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS


            The slot is for root constants.
          


### -field D3D12_ROOT_PARAMETER_TYPE_CBV


            The slot is for a constant-buffer view (CBV).
          


### -field D3D12_ROOT_PARAMETER_TYPE_SRV


            The slot is for a shader-resource view (SRV).
          


### -field D3D12_ROOT_PARAMETER_TYPE_UAV


            The slot is for a unordered-access view (UAV).
          


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/CC1DFE85-7F83-4551-86C6-1AFDF746FC92">D3D12_ROOT_PARAMETER</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/565B28C1-DBD1-42B6-87F9-70743E4A2E4A">Creating a Root Signature</a>
 

 

