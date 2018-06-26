---
UID: NS:d3d11.D3D11_BUFFER_DESC
title: D3D11_BUFFER_DESC
author: windows-sdk-content
description: Describes a buffer resource.
old-location: direct3d11\d3d11_buffer_desc.htm
old-project: direct3d11
ms.assetid: a5e470bb-011b-4a2a-96d6-cbf76fe12638
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D11_BUFFER_DESC, D3D11_BUFFER_DESC structure [Direct3D 11], d2dd6908-ed59-4009-c1dc-5afae3472d02, d3d11/D3D11_BUFFER_DESC, direct3d11.d3d11_buffer_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: D3D11_BUFFER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_BUFFER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_BUFFER_DESC structure


## -description


Describes a buffer resource.


## -struct-fields




### -field ByteWidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the buffer in bytes.


### -field Usage

Type: <b><a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a></b>

Identify how the buffer is expected to be read from and written to. Frequency of update is a key factor. The most common value is typically D3D11_USAGE_DEFAULT; see <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a> for all possible values.


### -field BindFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Identify how the buffer will be bound to the pipeline. Flags (see <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_FLAG</a>) can be combined with a logical OR.


### -field CPUAccessFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

CPU access flags (see <a href="https://msdn.microsoft.com/0a19c2a7-2570-40e2-8328-cbf5d7263605">D3D11_CPU_ACCESS_FLAG</a>) or 0 if no CPU access is necessary. Flags can be combined with a logical OR.


### -field MiscFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Miscellaneous flags (see <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_FLAG</a>) or 0 if unused. Flags can be combined with a logical OR.


### -field StructureByteStride

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of each element in the buffer structure (in bytes) when the buffer represents a structured buffer. For more info about structured buffers, see <a href="direct3d_11_advanced_stages_cs_resources.htm">Structured Buffer</a>.

The size value in <b>StructureByteStride</b> must match the size of the format that you use for views of the buffer. For example, if you use a shader resource view (SRV) to read a buffer in a pixel shader, the SRV format size must match the size value in <b>StructureByteStride</b>.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/5aec93c5-12a1-4b4e-813e-ee1e85adbf14">ID3D11Device::CreateBuffer</a> to create buffer resources.

In addition to this structure, you can also use the <a href="https://msdn.microsoft.com/A6ED5755-AB4A-4C35-A344-1693D78F7A4B">CD3D11_BUFFER_DESC</a> derived structure, which is defined  in D3D11.h and behaves like an inherited class, to help create a buffer description.

If the bind flag is <a href="d3d11_bind_flag.htm">D3D11_BIND_CONSTANT_BUFFER</a>, you must set the <b>ByteWidth</b> value in multiples of 16, and less than or equal to <b>D3D11_REQ_CONSTANT_BUFFER_ELEMENT_COUNT</b>.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

