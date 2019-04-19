---
UID: NF:d3d11.CD3D11_BUFFER_DESC.CD3D11_BUFFER_DESC(UINT,UINT,D3D11_USAGE,UINT,UINT,UINT)
title: CD3D11_BUFFER_DESC::CD3D11_BUFFER_DESC(UINT,UINT,D3D11_USAGE,UINT,UINT,UINT) (d3d11.h)
author: windows-sdk-content
description: Instantiates a new instance of a CD3D11_BUFFER_DESC structure that is initialized with D3D11_BUFFER_DESC values.
old-location: direct3d11\cd3d11_buffer_desc_cd3d11_buffer_desc_d3d11_buffer_desc_values_.htm
tech.root: direct3d11
ms.assetid: D0CC0B50-414A-4D19-A699-CCA007612EAF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CD3D11_BUFFER_DESC, CD3D11_BUFFER_DESC constructor [Direct3D 11], CD3D11_BUFFER_DESC constructor [Direct3D 11],CD3D11_BUFFER_DESC interface, CD3D11_BUFFER_DESC interface [Direct3D 11],CD3D11_BUFFER_DESC constructor, CD3D11_BUFFER_DESC.CD3D11_BUFFER_DESC, CD3D11_BUFFER_DESC.CD3D11_BUFFER_DESC(UINT,UINT,D3D11_USAGE,UINT,UINT,UINT), CD3D11_BUFFER_DESC::CD3D11_BUFFER_DESC, CD3D11_BUFFER_DESC::CD3D11_BUFFER_DESC(UINT,UINT,D3D11_USAGE,UINT,UINT,UINT), d3d11/CD3D11_BUFFER_DESC::CD3D11_BUFFER_DESC, direct3d11.cd3d11_buffer_desc_cd3d11_buffer_desc_d3d11_buffer_desc_values_
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - CD3D11_BUFFER_DESC.CD3D11_BUFFER_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CD3D11_BUFFER_DESC::CD3D11_BUFFER_DESC(UINT,UINT,D3D11_USAGE,UINT,UINT,UINT)


## -description


Instantiates a new instance of a <a href="https://msdn.microsoft.com/A6ED5755-AB4A-4C35-A344-1693D78F7A4B">CD3D11_BUFFER_DESC</a> structure that is initialized with <a href="https://msdn.microsoft.com/a5e470bb-011b-4a2a-96d6-cbf76fe12638">D3D11_BUFFER_DESC</a> values.


## -parameters




### -param byteWidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the buffer in bytes.


### -param bindFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_FLAG</a> values that are combined by using a bitwise OR operation. The resulting value identifies how the buffer will be bound to the pipeline.


### -param usage

Type: <b><a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a></b>

A <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a>-typed value that identifies how the buffer is expected to be read from and written to. Frequency of update is a key factor.


### -param cpuaccessFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/0a19c2a7-2570-40e2-8328-cbf5d7263605">D3D11_CPU_ACCESS_FLAG</a> values that are combined by using a bitwise OR operation or 0 if no CPU access is necessary. The resulting value identifies CPU access.


### -param miscFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_FLAG</a> values that are combined by using a bitwise OR operation or 0 if unused. The resulting value identifies miscellaneous buffer info.


### -param structureByteStride

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of each element in the buffer structure (in bytes) when the buffer represents a structured buffer. For more info about structured buffers, see <a href="https://msdn.microsoft.com/en-us/library/Ff476335(v=VS.85).aspx">Structured Buffer</a>.

The size value in <i>structureByteStride</i> must match the size of the format that you use for views of the buffer. For example, if you use a shader resource view (SRV) to read a buffer in a pixel shader, the SRV format size must match the size value in <i>structureByteStride</i>.


## -see-also




<a href="https://msdn.microsoft.com/A6ED5755-AB4A-4C35-A344-1693D78F7A4B">CD3D11_BUFFER_DESC</a>
 

 

