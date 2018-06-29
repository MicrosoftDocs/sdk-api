---
UID: NE:d3d11.D3D11_BUFFER_UAV_FLAG
title: D3D11_BUFFER_UAV_FLAG
author: windows-sdk-content
description: Identifies unordered-access view options for a buffer resource.
old-location: direct3d11\d3d11_buffer_uav_flag.htm
old-project: direct3d11
ms.assetid: 13cf0083-c61a-478d-94bd-00dec4cf27b7
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 5103c5e7-101e-9c1a-35cc-e3c97e30a9d5, D3D11_BUFFER_UAV_FLAG, D3D11_BUFFER_UAV_FLAG enumeration [Direct3D 11], D3D11_BUFFER_UAV_FLAG_APPEND, D3D11_BUFFER_UAV_FLAG_COUNTER, D3D11_BUFFER_UAV_FLAG_RAW, d3d11/D3D11_BUFFER_UAV_FLAG, d3d11/D3D11_BUFFER_UAV_FLAG_APPEND, d3d11/D3D11_BUFFER_UAV_FLAG_COUNTER, d3d11/D3D11_BUFFER_UAV_FLAG_RAW, direct3d11.d3d11_buffer_uav_flag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
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
tech.root: 
req.typenames: D3D11_BUFFER_UAV_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_BUFFER_UAV_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_BUFFER_UAV_FLAG enumeration


## -description


Identifies unordered-access view options for a buffer resource.


## -enum-fields




### -field D3D11_BUFFER_UAV_FLAG_RAW

Resource contains raw, unstructured data.  Requires the UAV format to be DXGI_FORMAT_R32_TYPELESS.
        For more info about raw viewing of buffers, see <a href="https://msdn.microsoft.com/library/Ff476900(v=VS.85).aspx">Raw Views of Buffers</a>.


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
 

 

