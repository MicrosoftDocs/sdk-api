---
UID: NE:d3d11.D3D11_QUERY_MISC_FLAG
title: D3D11_QUERY_MISC_FLAG (d3d11.h)
description: Flags that describe miscellaneous query behavior.
helpviewer_keywords: ["D3D11_QUERY_MISC_FLAG","D3D11_QUERY_MISC_FLAG enumeration [Direct3D 11]","D3D11_QUERY_MISC_PREDICATEHINT","d3d11/D3D11_QUERY_MISC_FLAG","d3d11/D3D11_QUERY_MISC_PREDICATEHINT","direct3d11.d3d11_query_misc_flag","f27525ae-a29c-15ac-7fd8-0d7cafc87209"]
old-location: direct3d11\d3d11_query_misc_flag.htm
tech.root: direct3d11
ms.assetid: a49a04f9-5804-43fb-b12d-f703721f4d30
ms.date: 12/05/2018
ms.keywords: D3D11_QUERY_MISC_FLAG, D3D11_QUERY_MISC_FLAG enumeration [Direct3D 11], D3D11_QUERY_MISC_PREDICATEHINT, d3d11/D3D11_QUERY_MISC_FLAG, d3d11/D3D11_QUERY_MISC_PREDICATEHINT, direct3d11.d3d11_query_misc_flag, f27525ae-a29c-15ac-7fd8-0d7cafc87209
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_QUERY_MISC_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_QUERY_MISC_FLAG
 - d3d11/D3D11_QUERY_MISC_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_QUERY_MISC_FLAG
---

# D3D11_QUERY_MISC_FLAG enumeration


## -description

Flags that describe miscellaneous query behavior.

## -enum-fields

### -field D3D11_QUERY_MISC_PREDICATEHINT:0x1

Tell the hardware that if it is not yet sure if something is hidden or not to draw it anyway. This is only used with an occlusion predicate. Predication data cannot be returned to your application via <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> when using this flag.

## -remarks

This flag is part of a query description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_desc">D3D11_QUERY_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
