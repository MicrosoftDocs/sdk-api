---
UID: NF:d3d11.ID3D11DeviceContext.GetResourceMinLOD
title: ID3D11DeviceContext::GetResourceMinLOD (d3d11.h)
description: Gets the minimum level-of-detail (LOD).
helpviewer_keywords: ["GetResourceMinLOD","GetResourceMinLOD method [Direct3D 11]","GetResourceMinLOD method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","GetResourceMinLOD method","ID3D11DeviceContext.GetResourceMinLOD","ID3D11DeviceContext::GetResourceMinLOD","d3d11/ID3D11DeviceContext::GetResourceMinLOD","direct3d11.id3d11devicecontext_getresourceminlod","ff23ef4d-444a-7056-36ac-50371c88186b"]
old-location: direct3d11\id3d11devicecontext_getresourceminlod.htm
tech.root: direct3d11
ms.assetid: 335f9394-064a-4a2c-b581-323a4a4fde70
ms.date: 12/05/2018
ms.keywords: GetResourceMinLOD, GetResourceMinLOD method [Direct3D 11], GetResourceMinLOD method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GetResourceMinLOD method, ID3D11DeviceContext.GetResourceMinLOD, ID3D11DeviceContext::GetResourceMinLOD, d3d11/ID3D11DeviceContext::GetResourceMinLOD, direct3d11.id3d11devicecontext_getresourceminlod, ff23ef4d-444a-7056-36ac-50371c88186b
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::GetResourceMinLOD
 - d3d11/ID3D11DeviceContext::GetResourceMinLOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.GetResourceMinLOD
---

# ID3D11DeviceContext::GetResourceMinLOD


## -description

Gets the minimum level-of-detail (LOD).

## -parameters

### -param pResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> which represents the resource.

## -returns

Type: <b>FLOAT</b>

Returns the minimum LOD.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>