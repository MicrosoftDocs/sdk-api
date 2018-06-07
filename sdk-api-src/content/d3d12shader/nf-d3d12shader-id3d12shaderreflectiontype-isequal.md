---
UID: NF:d3d12shader.ID3D12ShaderReflectionType.IsEqual
title: ID3D12ShaderReflectionType::IsEqual
author: windows-sdk-content
description: Indicates whether two ID3D12ShaderReflectionType Interface pointers have the same underlying type.
old-location: direct3d12\id3d12shaderreflectiontype_isequal.htm
old-project: direct3d12
ms.assetid: C1EAFAA2-6D35-4D4A-9153-98D927375EAD
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ID3D12ShaderReflectionType interface,IsEqual method, ID3D12ShaderReflectionType.IsEqual, ID3D12ShaderReflectionType::IsEqual, IsEqual, IsEqual method, IsEqual method,ID3D12ShaderReflectionType interface, d3d12shader/ID3D12ShaderReflectionType::IsEqual, direct3d12.id3d12shaderreflectiontype_isequal
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflectionType.IsEqual
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflectionType::IsEqual


## -description



          Indicates whether two <a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType Interface</a> pointers have the same underlying type.
        


## -parameters




### -param pType [in]

Type: <b><a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType Interface</a>.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            Returns S_OK if the pointers have the same underlying type; otherwise returns S_FALSE.
          




## -remarks



IsEqual indicates whether the sources of the <a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType Interface</a> pointers have the same underlying type.
        For example, if two <b>ID3D12ShaderReflectionType Interface</b> pointers were retrieved from variables, IsEqual can be used to see if
        the variables have the same type.
      


        This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType</a>
 

 

