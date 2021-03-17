---
UID: NF:d3d11shader.ID3D11Linker.Link
title: ID3D11Linker::Link (d3d11shader.h)
description: Links the shader and produces a shader blob that the Direct3D runtime can use.
helpviewer_keywords: ["ID3D11Linker interface [Direct3D 11]","Link method","ID3D11Linker.Link","ID3D11Linker::Link","Link","Link method [Direct3D 11]","Link method [Direct3D 11]","ID3D11Linker interface","d3d11shader/ID3D11Linker::Link","direct3d11.id3d11linker_link"]
old-location: direct3d11\id3d11linker_link.htm
tech.root: direct3d11
ms.assetid: FCEAE5C2-38E4-4B8F-BA98-F46B187FC586
ms.date: 12/05/2018
ms.keywords: ID3D11Linker interface [Direct3D 11],Link method, ID3D11Linker.Link, ID3D11Linker::Link, Link, Link method [Direct3D 11], Link method [Direct3D 11],ID3D11Linker interface, d3d11shader/ID3D11Linker::Link, direct3d11.id3d11linker_link
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
 - ID3D11Linker::Link
 - d3d11shader/ID3D11Linker::Link
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
 - ID3D11Linker.Link
---

# ID3D11Linker::Link


## -description

Links the shader and produces a shader blob that the Direct3D runtime can use.

## -parameters

### -param pEntry [in]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance">ID3D11ModuleInstance</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance">ID3D11ModuleInstance</a> interface for the shader module instance to link from.

### -param pEntryName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the shader module instance to link from.

### -param pTargetName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name for the shader blob that is produced.

### -param uFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Reserved.

### -param ppShaderBlob [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the compiled shader code.

### -param ppErrorBuffer [out, optional]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access compiler error messages.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker">ID3D11Linker</a>