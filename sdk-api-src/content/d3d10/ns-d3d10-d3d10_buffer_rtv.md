---
UID: NS:d3d10.D3D10_BUFFER_RTV
title: D3D10_BUFFER_RTV (d3d10.h)
description: Specifies the elements from a buffer resource to use in a render-target view.
helpviewer_keywords: ["4eb8f5a5-bb65-b551-7e42-ac051b09f97c","D3D10_BUFFER_RTV","D3D10_BUFFER_RTV structure [Direct3D 10]","d3d10/D3D10_BUFFER_RTV","direct3d10.d3d10_buffer_rtv"]
old-location: direct3d10\d3d10_buffer_rtv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_buffer_rtv.htm
ms.date: 12/05/2018
ms.keywords: 4eb8f5a5-bb65-b551-7e42-ac051b09f97c, D3D10_BUFFER_RTV, D3D10_BUFFER_RTV structure [Direct3D 10], d3d10/D3D10_BUFFER_RTV, direct3d10.d3d10_buffer_rtv
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
req.typenames: D3D10_BUFFER_RTV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_BUFFER_RTV
 - d3d10/D3D10_BUFFER_RTV
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
 - D3D10_BUFFER_RTV
---

# D3D10_BUFFER_RTV structure


## -description

Specifies the elements from a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffer</a> resource to use in a render-target view.

## -struct-fields

### -field FirstElement

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of bytes between the beginning of the buffer and the first element to access.

### -field ElementOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The offset of the first element in the view to access, relative to element 0.

### -field NumElements

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The total number of elements in the view.

### -field ElementWidth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The width of each element (in bytes). This can be determined from the format stored in the render-target-view description.

## -remarks

A render-target view is a member of a render-target-view description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_render_target_view_desc">D3D10_RENDER_TARGET_VIEW_DESC</a>). Create a render-target view by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrendertargetview">ID3D10Device::CreateRenderTargetView</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>