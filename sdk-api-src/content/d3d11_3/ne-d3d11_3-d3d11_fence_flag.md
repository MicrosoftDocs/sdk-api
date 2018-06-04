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

# D3D11_FENCE_FLAG enumeration


## -description



          Specifies fence options.
        


## -enum-fields




### -field D3D11_FENCE_FLAG_NONE


            No options are specified.
          


### -field D3D11_FENCE_FLAG_SHARED


            The fence is shared.
          


### -field D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER


            The fence is shared with another GPU adapter.
          


### -field D3D11_FENCE_FLAG_NON_MONITORED




## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/B4AA9E0D-AAF4-4632-A98F-A3212764D5E1">ID3D11Device::CreateFence</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

