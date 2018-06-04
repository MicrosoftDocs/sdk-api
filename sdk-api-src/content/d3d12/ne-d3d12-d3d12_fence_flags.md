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

# D3D12_FENCE_FLAGS enumeration


## -description



          Specifies fence options.
        


## -enum-fields




### -field D3D12_FENCE_FLAG_NONE


            No options are specified.
          


### -field D3D12_FENCE_FLAG_SHARED


            The fence is shared.
          


### -field D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER


            The fence is shared with another GPU adapter.
          


### -field D3D12_FENCE_FLAG_NON_MONITORED


            The fence is of the non-monitored type. Non-monitored fences should only be used when the adapter doesn't support monitored fences, or when a fence is shared with an adapter that doesn't support monitored fences.
          


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/731A60CA-644A-4FC2-8461-DDD686363BED">ID3D12Device::CreateFence</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

