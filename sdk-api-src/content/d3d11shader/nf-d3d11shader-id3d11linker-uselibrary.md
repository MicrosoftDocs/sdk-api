---
UID: NF:d3d11shader.ID3D11Linker.UseLibrary
title: ID3D11Linker::UseLibrary (d3d11shader.h)
description: Adds an instance of a library module to be used for linking.
helpviewer_keywords: ["ID3D11Linker interface [Direct3D 11]","UseLibrary method","ID3D11Linker.UseLibrary","ID3D11Linker::UseLibrary","UseLibrary","UseLibrary method [Direct3D 11]","UseLibrary method [Direct3D 11]","ID3D11Linker interface","d3d11shader/ID3D11Linker::UseLibrary","direct3d11.id3d11linker_uselibrary"]
old-location: direct3d11\id3d11linker_uselibrary.htm
tech.root: direct3d11
ms.assetid: 2FEA3583-8868-4763-8308-3C1E8F72A9BC
ms.date: 12/05/2018
ms.keywords: ID3D11Linker interface [Direct3D 11],UseLibrary method, ID3D11Linker.UseLibrary, ID3D11Linker::UseLibrary, UseLibrary, UseLibrary method [Direct3D 11], UseLibrary method [Direct3D 11],ID3D11Linker interface, d3d11shader/ID3D11Linker::UseLibrary, direct3d11.id3d11linker_uselibrary
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
 - ID3D11Linker::UseLibrary
 - d3d11shader/ID3D11Linker::UseLibrary
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
 - ID3D11Linker.UseLibrary
---

# ID3D11Linker::UseLibrary


## -description

Adds an instance of a library module to be used for linking.

## -parameters

### -param pLibraryMI [in]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance">ID3D11ModuleInstance</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance">ID3D11ModuleInstance</a> interface for the library module instance.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker">ID3D11Linker</a>