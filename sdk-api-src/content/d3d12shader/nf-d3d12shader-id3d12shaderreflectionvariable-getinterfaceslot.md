---
UID: NF:d3d12shader.ID3D12ShaderReflectionVariable.GetInterfaceSlot
title: ID3D12ShaderReflectionVariable::GetInterfaceSlot (d3d12shader.h)
description: Gets the corresponding interface slot for a variable that represents an interface pointer. (ID3D12ShaderReflectionVariable.GetInterfaceSlot)
helpviewer_keywords: ["GetInterfaceSlot","GetInterfaceSlot method","GetInterfaceSlot method","ID3D12ShaderReflectionVariable interface","ID3D12ShaderReflectionVariable interface","GetInterfaceSlot method","ID3D12ShaderReflectionVariable.GetInterfaceSlot","ID3D12ShaderReflectionVariable::GetInterfaceSlot","d3d12shader/ID3D12ShaderReflectionVariable::GetInterfaceSlot","direct3d12.id3d12shaderreflectionvariable_getinterfaceslot"]
old-location: direct3d12\id3d12shaderreflectionvariable_getinterfaceslot.htm
tech.root: direct3d12
ms.assetid: 6CD169C7-0C6B-4EC8-BF57-96EE5065CC9D
ms.date: 12/05/2018
ms.keywords: GetInterfaceSlot, GetInterfaceSlot method, GetInterfaceSlot method,ID3D12ShaderReflectionVariable interface, ID3D12ShaderReflectionVariable interface,GetInterfaceSlot method, ID3D12ShaderReflectionVariable.GetInterfaceSlot, ID3D12ShaderReflectionVariable::GetInterfaceSlot, d3d12shader/ID3D12ShaderReflectionVariable::GetInterfaceSlot, direct3d12.id3d12shaderreflectionvariable_getinterfaceslot
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12ShaderReflectionVariable::GetInterfaceSlot
 - d3d12shader/ID3D12ShaderReflectionVariable::GetInterfaceSlot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflectionVariable.GetInterfaceSlot
---

# ID3D12ShaderReflectionVariable::GetInterfaceSlot


## -description

Gets the corresponding interface slot for a variable that represents an interface pointer.

## -parameters

### -param uArrayIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the array element to get the slot number for.
            For a non-array variable this value will be zero.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Returns the index of the interface in the interface array.

## -remarks

GetInterfaceSlot gets the corresponding slot in a dynamic linkage array for an interface instance.
          The returned slot number is used to set an interface instance to a particular class instance.
          See the HLSL <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class">Interfaces and Classes</a> overview for additional information.
        

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable">ID3D12ShaderReflectionVariable</a>
