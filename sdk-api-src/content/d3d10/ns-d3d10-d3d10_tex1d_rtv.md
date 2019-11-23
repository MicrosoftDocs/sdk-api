---
UID: NS:d3d10.D3D10_TEX1D_RTV
title: D3D10_TEX1D_RTV (d3d10.h)

description: Specifies the subresource from a 1D texture to use in a render-target view.
old-location: direct3d10\d3d10_tex1d_rtv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex1d_rtv.htm

ms.date: 12/05/2018
ms.keywords: 591d1483-fde1-2aee-60bb-56aa133a09e4, D3D10_TEX1D_RTV, D3D10_TEX1D_RTV structure [Direct3D 10], d3d10/D3D10_TEX1D_RTV, direct3d10.d3d10_tex1d_rtv
ms.topic: struct
f1_keywords: 
 - "d3d10/D3D10_TEX1D_RTV"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_TEX1D_RTV
targetos: Windows
req.typenames: D3D10_TEX1D_RTV
req.redist: 
ms.custom: 19H1
---

# D3D10_TEX1D_RTV structure


## -description


Specifies the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> from a <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">1D texture</a> to use in a render-target view.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the mipmap level to use (see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">mip slice</a>).


## -remarks



This structure is one member of a render-target-view description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_render_target_view_desc">D3D10_RENDER_TARGET_VIEW_DESC</a>).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>
 

 

