---
UID: NF:d3dcompiler.D3DCreateBlob
title: D3DCreateBlob function (d3dcompiler.h)
description: Creates a buffer.
helpviewer_keywords: ["D3DCreateBlob","D3DCreateBlob function [HLSL]","d3dcompiler/D3DCreateBlob","direct3dhlsl.d3dcreateblob"]
old-location: direct3dhlsl\d3dcreateblob.htm
tech.root: direct3dhlsl
ms.assetid: 9cad9bff-1641-4fb1-a7c9-c3e31089d7f7
ms.date: 12/05/2018
ms.keywords: D3DCreateBlob, D3DCreateBlob function [HLSL], d3dcompiler/D3DCreateBlob, direct3dhlsl.d3dcreateblob
req.header: d3dcompiler.h
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
 - D3DCreateBlob
 - d3dcompiler/D3DCreateBlob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DCreateBlob
---

# D3DCreateBlob function


## -description

Creates a buffer.

## -parameters

### -param Size [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Number of bytes in the blob.

### -param ppBlob [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

The address of a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that is used to retrieve the buffer.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

The latest D3dcompiler_nn.dll contains the <b>D3DCreateBlob</b> compiler function. Therefore, you are no longer required to create and use an arbitrary length data buffer by using the  <a href="/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createblob">D3D10CreateBlob</a> function that is contained in D3d10.dll.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>