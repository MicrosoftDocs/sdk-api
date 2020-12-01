---
UID: NF:d3d11shader.ID3D11Module.CreateInstance
title: ID3D11Module::CreateInstance (d3d11shader.h)
description: Initializes an instance of a shader module that is used for resource rebinding.
helpviewer_keywords: ["CreateInstance","CreateInstance method [Direct3D 11]","CreateInstance method [Direct3D 11]","ID3D11Module interface","ID3D11Module interface [Direct3D 11]","CreateInstance method","ID3D11Module.CreateInstance","ID3D11Module::CreateInstance","d3d11shader/ID3D11Module::CreateInstance","direct3d11.id3d11module_createinstance"]
old-location: direct3d11\id3d11module_createinstance.htm
tech.root: direct3d11
ms.assetid: 737A69EF-F74E-4480-98EA-31D6CCAC0F8A
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Direct3D 11], CreateInstance method [Direct3D 11],ID3D11Module interface, ID3D11Module interface [Direct3D 11],CreateInstance method, ID3D11Module.CreateInstance, ID3D11Module::CreateInstance, d3d11shader/ID3D11Module::CreateInstance, direct3d11.id3d11module_createinstance
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
 - ID3D11Module::CreateInstance
 - d3d11shader/ID3D11Module::CreateInstance
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
 - ID3D11Module.CreateInstance
---

# ID3D11Module::CreateInstance


## -description

Initializes an instance of a shader module that is used for resource rebinding.

## -parameters

### -param pNamespace [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of a shader module to initialize. This can be <b>NULL</b> if you don't want to specify a name for the module.

### -param ppModuleInstance [out]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance">ID3D11ModuleInstance</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance">ID3D11ModuleInstance</a> interface to initialize.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module">ID3D11Module</a>