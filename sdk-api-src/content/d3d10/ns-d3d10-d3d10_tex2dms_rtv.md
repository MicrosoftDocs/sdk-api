---
UID: NS:d3d10.D3D10_TEX2DMS_RTV
title: D3D10_TEX2DMS_RTV (d3d10.h)
description: Specifies the subresource from a multisampled 2D texture to use in a render-target view. (D3D10_TEX2DMS_RTV)
helpviewer_keywords: ["D3D10_TEX2DMS_RTV","D3D10_TEX2DMS_RTV structure [Direct3D 10]","b35fccdd-d7a7-672b-7f33-80eef15788d6","d3d10/D3D10_TEX2DMS_RTV","direct3d10.d3d10_tex2dms_rtv"]
old-location: direct3d10\d3d10_tex2dms_rtv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2dms_rtv.htm
ms.date: 12/05/2018
ms.keywords: D3D10_TEX2DMS_RTV, D3D10_TEX2DMS_RTV structure [Direct3D 10], b35fccdd-d7a7-672b-7f33-80eef15788d6, d3d10/D3D10_TEX2DMS_RTV, direct3d10.d3d10_tex2dms_rtv
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
req.typenames: D3D10_TEX2DMS_RTV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_TEX2DMS_RTV
 - d3d10/D3D10_TEX2DMS_RTV
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
 - D3D10_TEX2DMS_RTV
---

# D3D10_TEX2DMS_RTV structure


## -description

Specifies the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> from a multisampled <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">2D texture</a> to use in a render-target view.

## -struct-fields

### -field UnusedField_NothingToDefine

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Integer of any value. See remarks.

## -remarks

Since a multisampled 2D texture contains a single subresource, there is actually nothing to specify in <b>D3D10_TEX2DMS_RTV</b>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>
