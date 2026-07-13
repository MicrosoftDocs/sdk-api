---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetThreadGroupSize
title: ID3D11ShaderReflection::GetThreadGroupSize (d3d11shader.h)
description: Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid. (ID3D11ShaderReflection.GetThreadGroupSize)
helpviewer_keywords: ["GetThreadGroupSize","GetThreadGroupSize method [Direct3D 11]","GetThreadGroupSize method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetThreadGroupSize method","ID3D11ShaderReflection.GetThreadGroupSize","ID3D11ShaderReflection::GetThreadGroupSize","d3d11shader/ID3D11ShaderReflection::GetThreadGroupSize","direct3d11.id3d11shaderreflection_getthreadgroupsize"]
old-location: direct3d11\id3d11shaderreflection_getthreadgroupsize.htm
tech.root: direct3d11
ms.assetid: e3f7b22d-75d6-4169-9336-26056c969195
ms.date: 12/05/2018
ms.keywords: GetThreadGroupSize, GetThreadGroupSize method [Direct3D 11], GetThreadGroupSize method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetThreadGroupSize method, ID3D11ShaderReflection.GetThreadGroupSize, ID3D11ShaderReflection::GetThreadGroupSize, d3d11shader/ID3D11ShaderReflection::GetThreadGroupSize, direct3d11.id3d11shaderreflection_getthreadgroupsize
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ShaderReflection::GetThreadGroupSize
 - d3d11shader/ID3D11ShaderReflection::GetThreadGroupSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflection.GetThreadGroupSize
---

# ID3D11ShaderReflection::GetThreadGroupSize


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
      

When a compute shader is written it defines the actions of a single thread group only. If multiple thread groups are required, it is the role of the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch">ID3D11DeviceContext::Dispatch</a> call to issue multiple thread groups.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection</a>
