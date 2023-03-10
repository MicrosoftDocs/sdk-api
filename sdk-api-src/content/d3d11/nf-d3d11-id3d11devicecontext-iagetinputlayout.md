---
UID: NF:d3d11.ID3D11DeviceContext.IAGetInputLayout
title: ID3D11DeviceContext::IAGetInputLayout (d3d11.h)
description: Get a pointer to the input-layout object that is bound to the input-assembler stage. (ID3D11DeviceContext.IAGetInputLayout)
helpviewer_keywords: ["833fde64-5672-81f0-24a0-876e6fb4fc29","IAGetInputLayout","IAGetInputLayout method [Direct3D 11]","IAGetInputLayout method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","IAGetInputLayout method","ID3D11DeviceContext.IAGetInputLayout","ID3D11DeviceContext::IAGetInputLayout","d3d11/ID3D11DeviceContext::IAGetInputLayout","direct3d11.id3d11devicecontext_iagetinputlayout"]
old-location: direct3d11\id3d11devicecontext_iagetinputlayout.htm
tech.root: direct3d11
ms.assetid: b3d07e01-405e-4973-956f-85a08b720aaa
ms.date: 12/05/2018
ms.keywords: 833fde64-5672-81f0-24a0-876e6fb4fc29, IAGetInputLayout, IAGetInputLayout method [Direct3D 11], IAGetInputLayout method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IAGetInputLayout method, ID3D11DeviceContext.IAGetInputLayout, ID3D11DeviceContext::IAGetInputLayout, d3d11/ID3D11DeviceContext::IAGetInputLayout, direct3d11.id3d11devicecontext_iagetinputlayout
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
 - ID3D11DeviceContext::IAGetInputLayout
 - d3d11/ID3D11DeviceContext::IAGetInputLayout
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
 - ID3D11DeviceContext.IAGetInputLayout
---

# ID3D11DeviceContext::IAGetInputLayout


## -description

Get a pointer to the input-layout object that is bound to the input-assembler stage.

## -parameters

### -param ppInputLayout [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout">ID3D11InputLayout</a>**</b>

A pointer to the input-layout object (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout">ID3D11InputLayout</a>), which describes the input buffers that will be read by the IA stage.

## -remarks

For information about creating an input-layout object, see Creating the Input-Layout Object.

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
