---
UID: NF:d3d11_1.ID3D11Device1.CreateRasterizerState1
title: ID3D11Device1::CreateRasterizerState1 (d3d11_1.h)
description: Creates a rasterizer state object that informs the rasterizer stage how to behave and forces the sample count while UAV rendering or rasterizing. (ID3D11Device1.CreateRasterizerState1)
helpviewer_keywords: ["CreateRasterizerState1","CreateRasterizerState1 method [Direct3D 11]","CreateRasterizerState1 method [Direct3D 11]","ID3D11Device1 interface","ID3D11Device1 interface [Direct3D 11]","CreateRasterizerState1 method","ID3D11Device1.CreateRasterizerState1","ID3D11Device1::CreateRasterizerState1","d3d11_1/ID3D11Device1::CreateRasterizerState1","direct3d11.id3d11device1_createrasterizerstate1"]
old-location: direct3d11\id3d11device1_createrasterizerstate1.htm
tech.root: direct3d11
ms.assetid: EBA793F1-35AA-4586-9D5C-803BD58B1D95
ms.date: 12/05/2018
ms.keywords: CreateRasterizerState1, CreateRasterizerState1 method [Direct3D 11], CreateRasterizerState1 method [Direct3D 11],ID3D11Device1 interface, ID3D11Device1 interface [Direct3D 11],CreateRasterizerState1 method, ID3D11Device1.CreateRasterizerState1, ID3D11Device1::CreateRasterizerState1, d3d11_1/ID3D11Device1::CreateRasterizerState1, direct3d11.id3d11device1_createrasterizerstate1
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11Device1::CreateRasterizerState1
 - d3d11_1/ID3D11Device1::CreateRasterizerState1
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
 - ID3D11Device1.CreateRasterizerState1
---

# ID3D11Device1::CreateRasterizerState1


## -description

Creates a rasterizer state object that informs the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> how to behave and forces the sample count while UAV rendering or rasterizing.

## -parameters

### -param pRasterizerDesc [in]

A pointer to a <a href="/windows/desktop/api/d3d11_1/ns-d3d11_1-cd3d11_rasterizer_desc1">D3D11_RASTERIZER_DESC1</a> structure that describes the  rasterizer state.

### -param ppRasterizerState [out, optional]

Address of a pointer to the <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11rasterizerstate1">ID3D11RasterizerState1</a> interface for the rasterizer state object created.

## -returns

This method returns E_OUTOFMEMORY if there is insufficient memory to create the rasterizer state object.  See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for other possible return values.

## -remarks

An app can create up to 4096 unique rasterizer state objects. For each object created, the runtime checks to see if a previous object 
      has the same state. If such a previous object exists, the runtime will return a pointer to previous instance instead of creating a duplicate object.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>
