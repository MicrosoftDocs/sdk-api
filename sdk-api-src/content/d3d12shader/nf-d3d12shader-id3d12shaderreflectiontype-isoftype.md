---
UID: NF:d3d12shader.ID3D12ShaderReflectionType.IsOfType
title: ID3D12ShaderReflectionType::IsOfType
author: windows-sdk-content
description: Indicates whether a variable is of the specified type.
old-location: direct3d12\id3d12shaderreflectiontype_isoftype.htm
tech.root: direct3d12
ms.assetid: 6B5A043A-927A-49AD-BF63-F8A9CCB57E09
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID3D12ShaderReflectionType interface,IsOfType method, ID3D12ShaderReflectionType.IsOfType, ID3D12ShaderReflectionType::IsOfType, IsOfType, IsOfType method, IsOfType method,ID3D12ShaderReflectionType interface, d3d12shader/ID3D12ShaderReflectionType::IsOfType, direct3d12.id3d12shaderreflectiontype_isoftype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12shader.h
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
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflectionType.IsOfType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12shader.h
: 
- ID3D12ShaderReflectionType.IsOfType
: 
---

# ID3D12ShaderReflectionType::IsOfType


## -description


Indicates whether a variable is of the specified type.
        


## -parameters




### -param pType [in]

Type: <b><a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType Interface</a>.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if object being queried is equal to or inherits from the type in the <i>pType</i> parameter; otherwise returns S_FALSE.
          




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType</a>
 

 

