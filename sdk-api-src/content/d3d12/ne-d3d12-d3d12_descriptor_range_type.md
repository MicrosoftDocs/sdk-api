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

# D3D12_DESCRIPTOR_RANGE_TYPE enumeration


## -description



          Specifies a range so that, for example, if part of a descriptor table has 100 shader-resource views (SRVs) that range can be declared in one entry rather than 100.
        


## -enum-fields




### -field D3D12_DESCRIPTOR_RANGE_TYPE_SRV


            Specifies a range of SRVs.
          


### -field D3D12_DESCRIPTOR_RANGE_TYPE_UAV


            Specifies a range of unordered-access views (UAVs).
          


### -field D3D12_DESCRIPTOR_RANGE_TYPE_CBV


            Specifies a range of constant-buffer views (CBVs).
          


### -field D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER


            Specifies a range of samplers.
          


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/6F1C4D05-3E08-4353-B5B9-4C4270FC1403">D3D12_DESCRIPTOR_RANGE</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

