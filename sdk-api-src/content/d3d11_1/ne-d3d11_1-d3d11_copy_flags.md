---
UID: NE:d3d11_1.D3D11_COPY_FLAGS
title: D3D11_COPY_FLAGS (d3d11_1.h)
description: Specifies how to handle the existing contents of a resource during a copy or update operation of a region within that resource.
helpviewer_keywords: ["D3D11_COPY_DISCARD","D3D11_COPY_FLAGS","D3D11_COPY_FLAGS enumeration [Direct3D 11]","D3D11_COPY_NO_OVERWRITE","d3d11_1/D3D11_COPY_DISCARD","d3d11_1/D3D11_COPY_FLAGS","d3d11_1/D3D11_COPY_NO_OVERWRITE","direct3d11.d3d11_copy_flags"]
old-location: direct3d11\d3d11_copy_flags.htm
tech.root: direct3d11
ms.assetid: 2141A053-931B-42F2-BC8C-AAE9F4739ED7
ms.date: 12/05/2018
ms.keywords: D3D11_COPY_DISCARD, D3D11_COPY_FLAGS, D3D11_COPY_FLAGS enumeration [Direct3D 11], D3D11_COPY_NO_OVERWRITE, d3d11_1/D3D11_COPY_DISCARD, d3d11_1/D3D11_COPY_FLAGS, d3d11_1/D3D11_COPY_NO_OVERWRITE, direct3d11.d3d11_copy_flags
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
req.typenames: D3D11_COPY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_COPY_FLAGS
 - d3d11_1/D3D11_COPY_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_1.h
api_name:
 - D3D11_COPY_FLAGS
---

# D3D11_COPY_FLAGS enumeration


## -description

<div class="alert"><b>Note</b>  This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Specifies how to handle the existing contents of a resource during a copy or update operation of a region within that resource.

## -enum-fields

### -field D3D11_COPY_NO_OVERWRITE:0x1

The existing contents of the resource cannot be overwritten.

### -field D3D11_COPY_DISCARD:0x2

The existing contents of the resource are undefined and can be discarded.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>



<a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1">ID3D11DeviceContext1::CopySubresourceRegion1</a>



<a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1">ID3D11DeviceContext1::UpdateSubresource1</a>
