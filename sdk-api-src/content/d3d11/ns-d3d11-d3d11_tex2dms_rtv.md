---
UID: NS:d3d11.D3D11_TEX2DMS_RTV
title: D3D11_TEX2DMS_RTV (d3d11.h)
description: Specifies the subresource from a multisampled 2D texture to use in a render-target view. (D3D11_TEX2DMS_RTV)
helpviewer_keywords: ["D3D11_TEX2DMS_RTV","D3D11_TEX2DMS_RTV structure [Direct3D 11]","b5ca8db8-f65e-f182-293c-40214b3b3994","d3d11/D3D11_TEX2DMS_RTV","direct3d11.d3d11_tex2dms_rtv"]
old-location: direct3d11\d3d11_tex2dms_rtv.htm
tech.root: direct3d11
ms.assetid: 5414183c-4abf-4030-a148-ade5c9213635
ms.date: 12/05/2018
ms.keywords: D3D11_TEX2DMS_RTV, D3D11_TEX2DMS_RTV structure [Direct3D 11], b5ca8db8-f65e-f182-293c-40214b3b3994, d3d11/D3D11_TEX2DMS_RTV, direct3d11.d3d11_tex2dms_rtv
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
req.typenames: D3D11_TEX2DMS_RTV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2DMS_RTV
 - d3d11/D3D11_TEX2DMS_RTV
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
 - D3D11_TEX2DMS_RTV
---

# D3D11_TEX2DMS_RTV structure


## -description

Specifies the subresource from a multisampled 2D texture to use in a render-target view.

## -struct-fields

### -field UnusedField_NothingToDefine

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Integer of any value. See remarks.

## -remarks

Since a multisampled 2D texture contains a single subresource, there is actually nothing to specify in D3D11_TEX2DMS_RTV. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
