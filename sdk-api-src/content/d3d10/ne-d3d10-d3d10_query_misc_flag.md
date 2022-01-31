---
UID: NE:d3d10.D3D10_QUERY_MISC_FLAG
title: D3D10_QUERY_MISC_FLAG (d3d10.h)
description: Flags that describe miscellaneous query behavior.
helpviewer_keywords: ["D3D10_QUERY_MISC_FLAG","D3D10_QUERY_MISC_FLAG enumeration [Direct3D 10]","D3D10_QUERY_MISC_PREDICATEHINT","afca49a1-e15e-21f0-d3cc-592d3ba4b0cd","d3d10/D3D10_QUERY_MISC_FLAG","d3d10/D3D10_QUERY_MISC_PREDICATEHINT","direct3d10.d3d10_query_misc_flag"]
old-location: direct3d10\d3d10_query_misc_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query_misc_flag.htm
ms.date: 12/05/2018
ms.keywords: D3D10_QUERY_MISC_FLAG, D3D10_QUERY_MISC_FLAG enumeration [Direct3D 10], D3D10_QUERY_MISC_PREDICATEHINT, afca49a1-e15e-21f0-d3cc-592d3ba4b0cd, d3d10/D3D10_QUERY_MISC_FLAG, d3d10/D3D10_QUERY_MISC_PREDICATEHINT, direct3d10.d3d10_query_misc_flag
req.header: d3d10.h
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
req.typenames: D3D10_QUERY_MISC_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_QUERY_MISC_FLAG
 - d3d10/D3D10_QUERY_MISC_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_QUERY_MISC_FLAG
---

# D3D10_QUERY_MISC_FLAG enumeration


## -description

Flags that describe miscellaneous query behavior.

## -enum-fields

### -field D3D10_QUERY_MISC_PREDICATEHINT:0x1

Tell the hardware that if it is not yet sure if something is hidden or not to draw it anyway. This is only used with an occlusion predicate. Predication data cannot be returned to your application via <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">ID3D10Asynchronous::GetData</a> when using this flag.

## -remarks

This flag is part of a query description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_query_desc">D3D10_QUERY_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
