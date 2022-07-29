---
UID: NF:d3d11shader.ID3D11LibraryReflection.GetDesc
title: ID3D11LibraryReflection::GetDesc (d3d11shader.h)
description: Fills the library descriptor structure for the library reflection. (ID3D11LibraryReflection.GetDesc)
helpviewer_keywords: ["GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11LibraryReflection interface","ID3D11LibraryReflection interface [Direct3D 11]","GetDesc method","ID3D11LibraryReflection.GetDesc","ID3D11LibraryReflection::GetDesc","d3d11shader/ID3D11LibraryReflection::GetDesc","direct3d11.id3d11libraryreflection_getdesc"]
old-location: direct3d11\id3d11libraryreflection_getdesc.htm
tech.root: direct3d11
ms.assetid: F23FEED8-94A3-4A87-8B4F-1D55BD47AF5F
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11LibraryReflection interface, ID3D11LibraryReflection interface [Direct3D 11],GetDesc method, ID3D11LibraryReflection.GetDesc, ID3D11LibraryReflection::GetDesc, d3d11shader/ID3D11LibraryReflection::GetDesc, direct3d11.id3d11libraryreflection_getdesc
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
 - ID3D11LibraryReflection::GetDesc
 - d3d11shader/ID3D11LibraryReflection::GetDesc
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
 - ID3D11LibraryReflection.GetDesc
---

# ID3D11LibraryReflection::GetDesc


## -description

Fills the library descriptor structure for the library reflection.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_library_desc">D3D11_LIBRARY_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_library_desc">D3D11_LIBRARY_DESC</a> structure that receives a description of the library reflection.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11libraryreflection">ID3D11LibraryReflection</a>
