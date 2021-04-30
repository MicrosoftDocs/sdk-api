---
UID: NF:d3d11.ID3D11ClassInstance.GetTypeName
title: ID3D11ClassInstance::GetTypeName (d3d11.h)
description: Gets the type of the current HLSL class.
helpviewer_keywords: ["37b4ce30-bd10-e500-268b-fcbfc22464f2","GetTypeName","GetTypeName method [Direct3D 11]","GetTypeName method [Direct3D 11]","ID3D11ClassInstance interface","ID3D11ClassInstance interface [Direct3D 11]","GetTypeName method","ID3D11ClassInstance.GetTypeName","ID3D11ClassInstance::GetTypeName","d3d11/ID3D11ClassInstance::GetTypeName","direct3d11.id3d11classinstance_gettypename"]
old-location: direct3d11\id3d11classinstance_gettypename.htm
tech.root: direct3d11
ms.assetid: a46699b5-2250-442a-85ab-37eeb419ac72
ms.date: 12/05/2018
ms.keywords: 37b4ce30-bd10-e500-268b-fcbfc22464f2, GetTypeName, GetTypeName method [Direct3D 11], GetTypeName method [Direct3D 11],ID3D11ClassInstance interface, ID3D11ClassInstance interface [Direct3D 11],GetTypeName method, ID3D11ClassInstance.GetTypeName, ID3D11ClassInstance::GetTypeName, d3d11/ID3D11ClassInstance::GetTypeName, direct3d11.id3d11classinstance_gettypename
req.header: d3d11.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ClassInstance::GetTypeName
 - d3d11/ID3D11ClassInstance::GetTypeName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11ClassInstance.GetTypeName
---

# ID3D11ClassInstance::GetTypeName


## -description

Gets the type of the current HLSL class.

## -parameters

### -param pTypeName [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPSTR</a></b>

Type of the current HLSL class.

### -param pBufferLength [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a>*</b>

The length of the <i>pTypeName</i> parameter.

## -remarks

GetTypeName will return a valid name only for instances acquired using <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance">ID3D11ClassLinkage::GetClassInstance</a>.
        

For more information about using the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a> interface, see <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking">Dynamic Linking</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>