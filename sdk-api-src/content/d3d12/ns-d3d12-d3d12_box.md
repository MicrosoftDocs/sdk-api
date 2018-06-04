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

# D3D12_BOX structure


## -description


Describes a 3D box.


## -struct-fields




### -field left

The x position of the left hand side of the box.


### -field top

The y position of the top of the box.


### -field front

The z position of the front of the box.


### -field right

The x position of the right hand side of the box, plus 1. This means that <code>right - left</code> equals the width of the box.


### -field bottom

The y position of the bottom of the box, plus 1. This means that <code>top - bottom</code> equals the height of the box.


### -field back

The z position of the back of the box, plus 1. This means that <code>front - back</code> equals the depth of the box.


## -remarks




        This structure is used by the methods <a href="https://msdn.microsoft.com/8781E2FE-8D82-41F5-B541-A96DA11CA290">WriteToSubresource</a>, <a href="https://msdn.microsoft.com/A1F61217-A383-49BF-B675-FBC7F6D015DB">ReadFromSubresource</a> and <a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/7E1A352C-D664-4538-BA78-91493980559D">CD3DX12_BOX</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

