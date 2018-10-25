---
UID: NF:d3d12.ID3D12PipelineLibrary.Serialize
title: ID3D12PipelineLibrary::Serialize
author: windows-sdk-content
description: Writes the contents of the library to the provided memory, to be provided back to the runtime at a later time.
old-location: direct3d12\id3d12pipelinelibrary_serialize.htm
tech.root: direct3d12
ms.assetid: FD81B464-1E93-47CF-9D95-8F8F64C39CD6
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID3D12PipelineLibrary interface,Serialize method, ID3D12PipelineLibrary.Serialize, ID3D12PipelineLibrary::Serialize, Serialize, Serialize method, Serialize method,ID3D12PipelineLibrary interface, d3d12/ID3D12PipelineLibrary::Serialize, direct3d12.id3d12pipelinelibrary_serialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12PipelineLibrary.Serialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12PipelineLibrary::Serialize


## -description


Writes the contents of the library to the provided memory, to be provided back to the runtime at a later time. 



## -parameters




### -param pData [out]

Type: <b>void*</b>

Specifies a pointer to the data. This memory must be readable and writeable up to the input size. This data can be saved and provided to <a href="https://msdn.microsoft.com/572A95A6-A02F-4512-9BDE-2A8CA58A0A27">CreatePipelineLibrary</a> at a later time, including future instances of this or other processes. The data becomes invalidated if the runtime or driver is updated, and is not portable to other hardware or devices.


### -param DataSizeInBytes

Type: <b>SIZE_T</b>

The size provided must be at least the size returned from <a href="https://msdn.microsoft.com/45DA092B-AB9B-43BE-8F5C-AE05485EA3C1">GetSerializedSize</a>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code, including E_INVALIDARG if the buffer provided isn’t big enough. 





## -remarks



Refer to the remarks and examples for <a href="https://msdn.microsoft.com/572A95A6-A02F-4512-9BDE-2A8CA58A0A27">CreatePipelineLibrary</a>. 




## -see-also




<a href="https://msdn.microsoft.com/7A1D750D-51F1-48F6-9D74-6439A147F1EC">ID3D12PipelineLibrary</a>
 

 

