---
UID: NS:d3d10.CD3D10_BUFFER_DESC
title: CD3D10_BUFFER_DESC
author: windows-sdk-content
description: Describes a buffer resource.
old-location: direct3d10\d3d10_buffer_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_buffer_desc.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 1eca8f2f-7776-2027-7a51-209cc4fd7200, CD3D10_BUFFER_DESC, D3D10_BUFFER_DESC, D3D10_BUFFER_DESC structure [Direct3D 10], d3d10/D3D10_BUFFER_DESC, direct3d10.d3d10_buffer_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
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
 - D3D10.h
api_name:
 - D3D10_BUFFER_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CD3D10_BUFFER_DESC structure


## -description


Describes a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">buffer</a> resource.


## -struct-fields




### -field D3D10_BUFFER_DESC

 




#### - BindFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Identify how the buffer will be bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205123(v=VS.85).aspx">pipeline</a>. Applications can logicaly OR flags together (see <a href="https://msdn.microsoft.com/en-us/library/Bb204891(v=VS.85).aspx">D3D10_BIND_FLAG</a>) to indicate that the buffer can be accessed in different ways.


#### - ByteWidth

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Size of the buffer in bytes.


#### - CPUAccessFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

CPU access flags (see <a href="https://msdn.microsoft.com/en-us/library/Bb204908(v=VS.85).aspx">D3D10_CPU_ACCESS_FLAG</a>) or 0 if no CPU access is necessary. Applications can logicaly OR flags together.


#### - MiscFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Miscellaneous flags (see <a href="https://msdn.microsoft.com/en-us/library/Bb172412(v=VS.85).aspx">D3D10_RESOURCE_MISC_FLAG</a>) or 0 if unused. Applications can logically OR flags together.


#### - Usage

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172499(v=VS.85).aspx">D3D10_USAGE</a></b>

Identify how the buffer is expected to be read from and written to. Frequency of update is a key factor. The most common value is typically D3D10_USAGE_DEFAULT; see <a href="https://msdn.microsoft.com/en-us/library/Bb172499(v=VS.85).aspx">D3D10_USAGE</a> for all possible values.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/en-us/library/Bb173544(v=VS.85).aspx">ID3D10Device::CreateBuffer</a> to create buffer resources.

In addition to this structure, there is also a derived structure in D3D10.h (CD3D10_BUFFER_DESC) which behaves like an inherited class to help create a buffer description.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

