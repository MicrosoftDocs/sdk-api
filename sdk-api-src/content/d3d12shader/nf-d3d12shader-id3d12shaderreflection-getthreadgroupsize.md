---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetThreadGroupSize
title: ID3D12ShaderReflection::GetThreadGroupSize (d3d12shader.h)
description: Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid. (ID3D12ShaderReflection.GetThreadGroupSize)
helpviewer_keywords: ["GetThreadGroupSize","GetThreadGroupSize method","GetThreadGroupSize method","ID3D12ShaderReflection interface","ID3D12ShaderReflection interface","GetThreadGroupSize method","ID3D12ShaderReflection.GetThreadGroupSize","ID3D12ShaderReflection::GetThreadGroupSize","d3d12shader/ID3D12ShaderReflection::GetThreadGroupSize","direct3d12.id3d12shaderreflection_getthreadgroupsize"]
old-location: direct3d12\id3d12shaderreflection_getthreadgroupsize.htm
tech.root: direct3d12
ms.assetid: C34A76B7-2410-4F0D-B2EC-8C62CD70DFE0
ms.date: 12/05/2018
ms.keywords: GetThreadGroupSize, GetThreadGroupSize method, GetThreadGroupSize method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetThreadGroupSize method, ID3D12ShaderReflection.GetThreadGroupSize, ID3D12ShaderReflection::GetThreadGroupSize, d3d12shader/ID3D12ShaderReflection::GetThreadGroupSize, direct3d12.id3d12shaderreflection_getthreadgroupsize
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
 - ID3D12ShaderReflection::GetThreadGroupSize
 - d3d12shader/ID3D12ShaderReflection::GetThreadGroupSize
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
 - ID3D12ShaderReflection.GetThreadGroupSize
---

# ID3D12ShaderReflection::GetThreadGroupSize


## -description

Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid.

## -parameters

### -param pSizeX [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to the size, in threads, of the x-dimension of the thread-group grid. The maximum size is 1024.

### -param pSizeY [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to the size, in threads, of the y-dimension of the thread-group grid. The maximum size is 1024.

### -param pSizeZ [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to the size, in threads, of the z-dimension of the thread-group grid. The maximum size is 64.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Returns the total size, in threads, of the thread-group grid by calculating the product of the size of each dimension.
            


``` syntax
*pSizeX * *pSizeY * *pSizeZ;
```


## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
        

When a compute shader is written it defines the actions of a single thread group only. If multiple thread groups are required, it is the role of the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch">ID3D12GraphicsCommandList::Dispatch</a> call to issue multiple thread groups.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection">ID3D12ShaderReflection</a>
