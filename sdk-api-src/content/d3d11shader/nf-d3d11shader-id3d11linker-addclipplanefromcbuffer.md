---
UID: NF:d3d11shader.ID3D11Linker.AddClipPlaneFromCBuffer
title: ID3D11Linker::AddClipPlaneFromCBuffer (d3d11shader.h)
description: Adds a clip plane with the plane coefficients taken from a cbuffer entry for 10Level9 shaders.
helpviewer_keywords: ["AddClipPlaneFromCBuffer","AddClipPlaneFromCBuffer method [Direct3D 11]","AddClipPlaneFromCBuffer method [Direct3D 11]","ID3D11Linker interface","ID3D11Linker interface [Direct3D 11]","AddClipPlaneFromCBuffer method","ID3D11Linker.AddClipPlaneFromCBuffer","ID3D11Linker::AddClipPlaneFromCBuffer","d3d11shader/ID3D11Linker::AddClipPlaneFromCBuffer","direct3d11.id3d11linker_addclipplanefromcbuffer"]
old-location: direct3d11\id3d11linker_addclipplanefromcbuffer.htm
tech.root: direct3d11
ms.assetid: 0E7820F1-8F4E-43B2-A8DD-560BC2B5BC3D
ms.date: 12/05/2018
ms.keywords: AddClipPlaneFromCBuffer, AddClipPlaneFromCBuffer method [Direct3D 11], AddClipPlaneFromCBuffer method [Direct3D 11],ID3D11Linker interface, ID3D11Linker interface [Direct3D 11],AddClipPlaneFromCBuffer method, ID3D11Linker.AddClipPlaneFromCBuffer, ID3D11Linker::AddClipPlaneFromCBuffer, d3d11shader/ID3D11Linker::AddClipPlaneFromCBuffer, direct3d11.id3d11linker_addclipplanefromcbuffer
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
 - ID3D11Linker::AddClipPlaneFromCBuffer
 - d3d11shader/ID3D11Linker::AddClipPlaneFromCBuffer
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
 - ID3D11Linker.AddClipPlaneFromCBuffer
---

# ID3D11Linker::AddClipPlaneFromCBuffer


## -description

Adds a <a href="/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9">clip plane</a> with the plane coefficients taken from a <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-constants">cbuffer</a> entry for 10Level9 shaders.

## -parameters

### -param uCBufferSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-constants">cbuffer</a> slot number.

### -param uCBufferEntry [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-constants">cbuffer</a> entry number.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker">ID3D11Linker</a>