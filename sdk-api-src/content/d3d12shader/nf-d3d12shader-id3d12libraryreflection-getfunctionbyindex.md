---
UID: NF:d3d12shader.ID3D12LibraryReflection.GetFunctionByIndex
title: ID3D12LibraryReflection::GetFunctionByIndex (d3d12shader.h)
description: The ID3D12LibraryReflection::GetFunctionByIndex method (d3d12shader.h) gets the function reflector.
helpviewer_keywords: ["GetFunctionByIndex","GetFunctionByIndex method","GetFunctionByIndex method","ID3D12LibraryReflection interface","ID3D12LibraryReflection interface","GetFunctionByIndex method","ID3D12LibraryReflection.GetFunctionByIndex","ID3D12LibraryReflection::GetFunctionByIndex","d3d12shader/ID3D12LibraryReflection::GetFunctionByIndex","direct3d12.id3d12libraryreflection_getfunctionbyindex"]
old-location: direct3d12\id3d12libraryreflection_getfunctionbyindex.htm
tech.root: direct3d12
ms.assetid: 1600824A-6C9E-4C87-8D6B-07F299D47A53
ms.date: 08/10/2022
ms.keywords: GetFunctionByIndex, GetFunctionByIndex method, GetFunctionByIndex method,ID3D12LibraryReflection interface, ID3D12LibraryReflection interface,GetFunctionByIndex method, ID3D12LibraryReflection.GetFunctionByIndex, ID3D12LibraryReflection::GetFunctionByIndex, d3d12shader/ID3D12LibraryReflection::GetFunctionByIndex, direct3d12.id3d12libraryreflection_getfunctionbyindex
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
 - ID3D12LibraryReflection::GetFunctionByIndex
 - d3d12shader/ID3D12LibraryReflection::GetFunctionByIndex
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
 - ID3D12LibraryReflection.GetFunctionByIndex
---

# ID3D12LibraryReflection::GetFunctionByIndex


## -description

Gets the function reflector.

## -parameters

### -param FunctionIndex [in]

Type: <b>INT</b>

The zero-based index of the function reflector to retrieve.

## -returns

Type: <b><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection">ID3D12FunctionReflection</a>*</b>

The function reflector, as a pointer to <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection">ID3D12FunctionReflection</a>.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection">ID3D12LibraryReflection</a>