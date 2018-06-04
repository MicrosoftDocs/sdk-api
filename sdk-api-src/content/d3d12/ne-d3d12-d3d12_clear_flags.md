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

# D3D12_CLEAR_FLAGS enumeration


## -description


Specifies what to clear from the depth stencil view.


## -enum-fields




### -field D3D12_CLEAR_FLAG_DEPTH

Indicates the depth buffer should be cleared.


### -field D3D12_CLEAR_FLAG_STENCIL

Indicates the stencil buffer should be cleared.


## -remarks




          This enum is used by <a href="https://msdn.microsoft.com/EF56EA6C-00DB-4231-B67D-B99811F51246">ID3D12GraphicsCommandList::ClearDepthStencilView</a>.
          The flags can be combined to clear all.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

