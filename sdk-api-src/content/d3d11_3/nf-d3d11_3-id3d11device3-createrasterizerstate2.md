---
UID: NF:d3d11_3.ID3D11Device3.CreateRasterizerState2
title: ID3D11Device3::CreateRasterizerState2 (d3d11_3.h)
description: Creates a rasterizer state object that informs the rasterizer stage how to behave and forces the sample count while UAV rendering or rasterizing. (ID3D11Device3.CreateRasterizerState2)
helpviewer_keywords: ["CreateRasterizerState2","CreateRasterizerState2 method [Direct3D 11]","CreateRasterizerState2 method [Direct3D 11]","ID3D11Device3 interface","ID3D11Device3 interface [Direct3D 11]","CreateRasterizerState2 method","ID3D11Device3.CreateRasterizerState2","ID3D11Device3::CreateRasterizerState2","d3d11_3/ID3D11Device3::CreateRasterizerState2","direct3d11.id3d11device3_createrasterizerstate2"]
old-location: direct3d11\id3d11device3_createrasterizerstate2.htm
tech.root: direct3d11
ms.assetid: 42BA8F50-7D86-4411-AE05-74F492761DBD
ms.date: 12/05/2018
ms.keywords: CreateRasterizerState2, CreateRasterizerState2 method [Direct3D 11], CreateRasterizerState2 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],CreateRasterizerState2 method, ID3D11Device3.CreateRasterizerState2, ID3D11Device3::CreateRasterizerState2, d3d11_3/ID3D11Device3::CreateRasterizerState2, direct3d11.id3d11device3_createrasterizerstate2
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D11Device3::CreateRasterizerState2
 - d3d11_3/ID3D11Device3::CreateRasterizerState2
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
 - ID3D11Device3.CreateRasterizerState2
---

# ID3D11Device3::CreateRasterizerState2


## -description

Creates a rasterizer state object that informs the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> how to behave and forces the sample count while UAV rendering or rasterizing.

## -parameters

### -param pRasterizerDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-cd3d11_rasterizer_desc2">D3D11_RASTERIZER_DESC2</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-cd3d11_rasterizer_desc2">D3D11_RASTERIZER_DESC2</a> structure that describes the  rasterizer state.

### -param ppRasterizerState [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11rasterizerstate2">ID3D11RasterizerState2</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11rasterizerstate2">ID3D11RasterizerState2</a> interface for the created rasterizer state object. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the rasterizer state object.  See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for other possible return values.

## -see-also

<a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11device3">ID3D11Device3</a>
