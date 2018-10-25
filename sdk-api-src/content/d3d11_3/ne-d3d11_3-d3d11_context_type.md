---
UID: NE:d3d11_3.D3D11_CONTEXT_TYPE
title: D3D11_CONTEXT_TYPE
author: windows-sdk-content
description: Specifies the context in which a query occurs.
old-location: direct3d11\d3d11_context_type.htm
tech.root: direct3d11
ms.assetid: 5467F07C-E429-4324-B52E-FDC25B4DB9FE
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_CONTEXT_TYPE, D3D11_CONTEXT_TYPE enumeration [Direct3D 11], D3D11_CONTEXT_TYPE_3D, D3D11_CONTEXT_TYPE_ALL, D3D11_CONTEXT_TYPE_COMPUTE, D3D11_CONTEXT_TYPE_COPY, D3D11_CONTEXT_TYPE_VIDEO, d3d11_3/D3D11_CONTEXT_TYPE, d3d11_3/D3D11_CONTEXT_TYPE_3D, d3d11_3/D3D11_CONTEXT_TYPE_ALL, d3d11_3/D3D11_CONTEXT_TYPE_COMPUTE, d3d11_3/D3D11_CONTEXT_TYPE_COPY, d3d11_3/D3D11_CONTEXT_TYPE_VIDEO, direct3d11.d3d11_context_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11_3.h
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
 - D3D11_3.h
api_name:
 - D3D11_CONTEXT_TYPE
product: Windows
targetos: Windows
req.typenames: D3D11_CONTEXT_TYPE
req.redist: 
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
<li>A CD3D11_QUERY_DESC1 constructor.</li>
<li>
<a href="https://msdn.microsoft.com/DBDA19C3-EC4E-4C12-B1ED-A92E5CE28CED">ID3D11DeviceContext3::Flush1</a> method
          </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>



<a href="https://msdn.microsoft.com/56FFA63E-E7C6-45A4-80E9-B12E9042AE13">D3D11_QUERY_DESC1</a>
 

 

