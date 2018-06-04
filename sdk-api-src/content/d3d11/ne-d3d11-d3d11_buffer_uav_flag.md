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

# D3D11_BUFFER_UAV_FLAG enumeration


## -description


Identifies unordered-access view options for a buffer resource.


## -enum-fields




### -field D3D11_BUFFER_UAV_FLAG_RAW

Resource contains raw, unstructured data.  Requires the UAV format to be DXGI_FORMAT_R32_TYPELESS.
        For more info about raw viewing of buffers, see <a href="overviews_direct3d_11_resources_intro.htm">Raw Views of Buffers</a>.


### -field D3D11_BUFFER_UAV_FLAG_APPEND

Allow data to be appended to the end of the buffer.  <b>D3D11_BUFFER_UAV_FLAG_APPEND</b> flag must also be used for 
        any view that will be used as a <a href="https://msdn.microsoft.com/377b0358-0f9d-4021-9140-19c3d1bfed38">AppendStructuredBuffer</a> or a <a href="https://msdn.microsoft.com/373bdd97-6186-4bce-99bf-738a153234f6">ConsumeStructuredBuffer</a>. 
        Requires the UAV format to be DXGI_FORMAT_UNKNOWN.


### -field D3D11_BUFFER_UAV_FLAG_COUNTER

Adds a counter to the unordered-access-view buffer.  <b>D3D11_BUFFER_UAV_FLAG_COUNTER</b> can only be used on a UAV that is a 
        <a href="https://msdn.microsoft.com/8dd93b81-135d-4f28-898f-38510dc39af1">RWStructuredBuffer</a> and it enables the functionality needed for the <a href="https://msdn.microsoft.com/66385d4f-6db8-49ae-a73a-49089695f5ee">IncrementCounter</a>
        and <a href="https://msdn.microsoft.com/24bc0b63-a482-4fa5-9898-2d43bca20cf4">DecrementCounter</a> methods in HLSL.  Requires the UAV format to be DXGI_FORMAT_UNKNOWN.


## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>



<a href="https://msdn.microsoft.com/b547819b-7006-40b5-84a4-adf198048051">Resource Enumerations</a>
 

 

