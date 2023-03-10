---
UID: NF:d3d11shader.ID3D11LibraryReflection.GetFunctionByIndex
title: ID3D11LibraryReflection::GetFunctionByIndex (d3d11shader.h)
description: The ID3D11LibraryReflection::GetFunctionByIndex (d3d11shader.h) method gets the function reflector.
helpviewer_keywords: ["GetFunctionByIndex","GetFunctionByIndex method [Direct3D 11]","GetFunctionByIndex method [Direct3D 11]","ID3D11LibraryReflection interface","ID3D11LibraryReflection interface [Direct3D 11]","GetFunctionByIndex method","ID3D11LibraryReflection.GetFunctionByIndex","ID3D11LibraryReflection::GetFunctionByIndex","d3d11shader/ID3D11LibraryReflection::GetFunctionByIndex","direct3d11.id3d11libraryreflection_getfunctionbyindex"]
old-location: direct3d11\id3d11libraryreflection_getfunctionbyindex.htm
tech.root: direct3d11
ms.assetid: 3058CCB5-E58E-4EEC-AEB9-C47B78DD6E79
ms.date: 08/10/2022
ms.keywords: GetFunctionByIndex, GetFunctionByIndex method [Direct3D 11], GetFunctionByIndex method [Direct3D 11],ID3D11LibraryReflection interface, ID3D11LibraryReflection interface [Direct3D 11],GetFunctionByIndex method, ID3D11LibraryReflection.GetFunctionByIndex, ID3D11LibraryReflection::GetFunctionByIndex, d3d11shader/ID3D11LibraryReflection::GetFunctionByIndex, direct3d11.id3d11libraryreflection_getfunctionbyindex
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
 - ID3D11LibraryReflection::GetFunctionByIndex
 - d3d11shader/ID3D11LibraryReflection::GetFunctionByIndex
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
 - ID3D11LibraryReflection.GetFunctionByIndex
---

# ID3D11LibraryReflection::GetFunctionByIndex


## -description

Gets the function reflector.

## -parameters

### -param FunctionIndex [in]

Type: <b>INT</b>

The zero-based index of the function reflector to retrieve.

## -returns

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionreflection">ID3D11FunctionReflection</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionreflection">ID3D11FunctionReflection</a> interface that represents the function reflector.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11libraryreflection">ID3D11LibraryReflection</a>