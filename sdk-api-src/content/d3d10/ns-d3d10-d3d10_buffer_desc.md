---
UID: NS:d3d10.D3D10_BUFFER_DESC
title: D3D10_BUFFER_DESC
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
req.typenames: D3D10_BUFFER_DESC
req.redist: 
---

# D3D10_BUFFER_DESC structure


## -description


Describes a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">buffer</a> resource.


## -struct-fields




#### - ByteWidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the buffer in bytes.


#### - Usage

Type: <b><a href="https://msdn.microsoft.com/eaaf695c-e99d-4bf8-b479-fa2d06d53248">D3D10_USAGE</a></b>

Identify how the buffer is expected to be read from and written to. Frequency of update is a key factor. The most common value is typically D3D10_USAGE_DEFAULT; see <a href="https://msdn.microsoft.com/eaaf695c-e99d-4bf8-b479-fa2d06d53248">D3D10_USAGE</a> for all possible values.


#### - BindFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Identify how the buffer will be bound to the <a href="https://msdn.microsoft.com/3ead6c7c-c7cc-48f1-81d5-b4b67326d610">pipeline</a>. Applications can logicaly OR flags together (see <a href="https://msdn.microsoft.com/3bbefc3b-ad05-499b-bbec-f370bf08a7f4">D3D10_BIND_FLAG</a>) to indicate that the buffer can be accessed in different ways.


#### - CPUAccessFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

CPU access flags (see <a href="https://msdn.microsoft.com/0f3dfe49-f4e0-4a66-a6f7-47170b0daa0b">D3D10_CPU_ACCESS_FLAG</a>) or 0 if no CPU access is necessary. Applications can logicaly OR flags together.


#### - MiscFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Miscellaneous flags (see <a href="https://msdn.microsoft.com/bdcb4e87-0285-4e96-a7ce-e08a43d3a4cb">D3D10_RESOURCE_MISC_FLAG</a>) or 0 if unused. Applications can logically OR flags together.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/77e943f7-f347-4d04-8e2e-a678d5a2c81c">ID3D10Device::CreateBuffer</a> to create buffer resources.

In addition to this structure, there is also a derived structure in D3D10.h (CD3D10_BUFFER_DESC) which behaves like an inherited class to help create a buffer description.




## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

