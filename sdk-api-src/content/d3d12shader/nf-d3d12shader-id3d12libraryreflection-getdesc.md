---
UID: NF:d3d12shader.ID3D12LibraryReflection.GetDesc
title: ID3D12LibraryReflection::GetDesc (d3d12shader.h)
description: Fills the library descriptor structure for the library reflection. (ID3D12LibraryReflection.GetDesc)
helpviewer_keywords: ["GetDesc","GetDesc method","GetDesc method","ID3D12LibraryReflection interface","ID3D12LibraryReflection interface","GetDesc method","ID3D12LibraryReflection.GetDesc","ID3D12LibraryReflection::GetDesc","d3d12shader/ID3D12LibraryReflection::GetDesc","direct3d12.id3d12libraryreflection_getdesc"]
old-location: direct3d12\id3d12libraryreflection_getdesc.htm
tech.root: direct3d12
ms.assetid: BF7CC078-3F68-4645-B49C-1F4DEBCA6A48
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method, GetDesc method,ID3D12LibraryReflection interface, ID3D12LibraryReflection interface,GetDesc method, ID3D12LibraryReflection.GetDesc, ID3D12LibraryReflection::GetDesc, d3d12shader/ID3D12LibraryReflection::GetDesc, direct3d12.id3d12libraryreflection_getdesc
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
 - ID3D12LibraryReflection::GetDesc
 - d3d12shader/ID3D12LibraryReflection::GetDesc
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
 - ID3D12LibraryReflection.GetDesc
---

# ID3D12LibraryReflection::GetDesc


## -description

Fills the library descriptor structure for the library reflection.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_library_desc">D3D12_LIBRARY_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_library_desc">D3D12_LIBRARY_DESC</a> structure that receives a description of the library reflection.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection">ID3D12LibraryReflection</a>
