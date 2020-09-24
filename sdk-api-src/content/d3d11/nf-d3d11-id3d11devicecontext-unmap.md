---
UID: NF:d3d11.ID3D11DeviceContext.Unmap
title: ID3D11DeviceContext::Unmap (d3d11.h)
description: Invalidate the pointer to a resource and reenable the GPU's access to that resource.
helpviewer_keywords: ["83629121-3205-9ee6-6495-a815e1ef2ab5","ID3D11DeviceContext interface [Direct3D 11]","Unmap method","ID3D11DeviceContext.Unmap","ID3D11DeviceContext::Unmap","Unmap","Unmap method [Direct3D 11]","Unmap method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::Unmap","direct3d11.id3d11devicecontext_unmap"]
old-location: direct3d11\id3d11devicecontext_unmap.htm
tech.root: direct3d11
ms.assetid: 67797b77-c0a5-47b4-ba54-4282b6aa5b13
ms.date: 12/05/2018
ms.keywords: 83629121-3205-9ee6-6495-a815e1ef2ab5, ID3D11DeviceContext interface [Direct3D 11],Unmap method, ID3D11DeviceContext.Unmap, ID3D11DeviceContext::Unmap, Unmap, Unmap method [Direct3D 11], Unmap method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::Unmap, direct3d11.id3d11devicecontext_unmap
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
 - ID3D11DeviceContext::Unmap
 - d3d11/ID3D11DeviceContext::Unmap
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
 - ID3D11DeviceContext.Unmap
---

# ID3D11DeviceContext::Unmap


## -description

Invalidate the pointer to a resource and reenable the GPU's access to that resource.

## -parameters

### -param pResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> interface.

### -param Subresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A subresource to be unmapped.

## -remarks

For info about how to use <b>Unmap</b>, see <a href="/windows/desktop/direct3d11/how-to--use-dynamic-resources">How to: Use dynamic resources</a>.
      

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>