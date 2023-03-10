---
UID: NF:d3d11_1.ID3D11DeviceContext1.DiscardResource
title: ID3D11DeviceContext1::DiscardResource (d3d11_1.h)
description: Discards a resource from the device context.
helpviewer_keywords: ["DiscardResource","DiscardResource method [Direct3D 11]","DiscardResource method [Direct3D 11]","ID3D11DeviceContext1 interface","ID3D11DeviceContext1 interface [Direct3D 11]","DiscardResource method","ID3D11DeviceContext1.DiscardResource","ID3D11DeviceContext1::DiscardResource","d3d11_1/ID3D11DeviceContext1::DiscardResource","direct3d11.id3d11devicecontext1_discardresource"]
old-location: direct3d11\id3d11devicecontext1_discardresource.htm
tech.root: direct3d11
ms.assetid: 6C27231E-BF61-4D50-B5B1-59961B82534B
ms.date: 12/05/2018
ms.keywords: DiscardResource, DiscardResource method [Direct3D 11], DiscardResource method [Direct3D 11],ID3D11DeviceContext1 interface, ID3D11DeviceContext1 interface [Direct3D 11],DiscardResource method, ID3D11DeviceContext1.DiscardResource, ID3D11DeviceContext1::DiscardResource, d3d11_1/ID3D11DeviceContext1::DiscardResource, direct3d11.id3d11devicecontext1_discardresource
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
 - ID3D11DeviceContext1::DiscardResource
 - d3d11_1/ID3D11DeviceContext1::DiscardResource
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
 - ID3D11DeviceContext1.DiscardResource
---

# ID3D11DeviceContext1::DiscardResource


## -description

Discards a resource from the device context.

## -parameters

### -param pResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> interface for the resource to discard. The resource must have been created with usage <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DEFAULT</a> or <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DYNAMIC</a>, otherwise the runtime drops the call to <b>DiscardResource</b>; if the debug layer is enabled, the runtime returns an error message.

## -remarks

<b>DiscardResource</b> informs the graphics processing unit (GPU) that the existing content in the resource that <i>pResource</i> points to is no longer needed.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>