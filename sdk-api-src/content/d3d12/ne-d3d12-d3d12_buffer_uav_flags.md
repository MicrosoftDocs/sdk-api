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

# D3D12_BUFFER_UAV_FLAGS enumeration


## -description


Identifies unordered-access view options for a buffer resource.


## -enum-fields




### -field D3D12_BUFFER_UAV_FLAG_NONE


            Indicates a default view.
          


### -field D3D12_BUFFER_UAV_FLAG_RAW


            Resource contains raw, unstructured data.  Requires the UAV format to be <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R32_TYPELESS</a>.
            For more info about raw viewing of buffers, see <a href="https://msdn.microsoft.com/9e991ab0-9648-484a-9a2c-5391ee5abf20">Raw Views of Buffers</a>.
          


## -remarks




        This enum is used in the <a href="https://msdn.microsoft.com/13E48B8F-4EF7-45B7-88F2-61D9BA1801D2">D3D12_BUFFER_UAV</a>  structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

