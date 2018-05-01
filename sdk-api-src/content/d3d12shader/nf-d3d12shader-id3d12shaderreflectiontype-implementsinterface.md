---
UID: NF:d3d12shader.ID3D12ShaderReflectionType.ImplementsInterface
title: ID3D12ShaderReflectionType::ImplementsInterface method
author: windows-driver-content
description: Indicates whether a class type implements an interface.
old-location: direct3d12\id3d12shaderreflectiontype_implementsinterface.htm
old-project: direct3d12
ms.assetid: FE84D58A-998D-4362-96B2-5C00D2A82CB8
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ID3D12ShaderReflectionType, ID3D12ShaderReflectionType interface, ImplementsInterface method, ID3D12ShaderReflectionType::ImplementsInterface, ImplementsInterface method, ImplementsInterface method, ID3D12ShaderReflectionType interface, ImplementsInterface,ID3D12ShaderReflectionType.ImplementsInterface, d3d12shader/ID3D12ShaderReflectionType::ImplementsInterface, direct3d12.id3d12shaderreflectiontype_implementsinterface
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
req.typenames: D3D12_SHADER_VERSION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12shader.h
api_name:
-	ID3D12ShaderReflectionType.ImplementsInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflectionType::ImplementsInterface method


## -description



          Indicates whether a class type implements an interface.
        


## -parameters




### -param pBase [in]

Type: <b><a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType Interface</a>.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            Returns S_OK if the interface is implemented; otherwise return S_FALSE.
          




## -remarks




        This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/78FF30C5-7F23-489D-9E9D-916F6CE09C0E">ID3D12ShaderReflectionType</a>
 

 

