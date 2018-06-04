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

# D3D11_CONTEXT_TYPE enumeration


## -description


Specifies the context in which a query occurs.


## -enum-fields




### -field D3D11_CONTEXT_TYPE_ALL

The query can occur in all contexts.


### -field D3D11_CONTEXT_TYPE_3D

The query occurs in the context of a 3D command queue.


### -field D3D11_CONTEXT_TYPE_COMPUTE

The query occurs in the context of a 3D compute queue.


### -field D3D11_CONTEXT_TYPE_COPY

The query occurs in the context of a 3D copy queue.


### -field D3D11_CONTEXT_TYPE_VIDEO

The query occurs in the context of video.


## -remarks




        This enum is used by the following:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/56FFA63E-E7C6-45A4-80E9-B12E9042AE13">D3D11_QUERY_DESC1</a> structure
          </li>
<li>
            A CD3D11_QUERY_DESC1 constructor.</li>
<li>
<a href="https://msdn.microsoft.com/DBDA19C3-EC4E-4C12-B1ED-A92E5CE28CED">ID3D11DeviceContext3::Flush1</a> method
          </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>



<a href="https://msdn.microsoft.com/56FFA63E-E7C6-45A4-80E9-B12E9042AE13">D3D11_QUERY_DESC1</a>
 

 

