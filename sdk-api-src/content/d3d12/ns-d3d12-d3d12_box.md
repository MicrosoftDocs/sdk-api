---
UID: NS:d3d12.D3D12_BOX
title: D3D12_BOX (d3d12.h)
description: Describes a 3D box.
helpviewer_keywords: ["D3D12_BOX","D3D12_BOX structure","d3d12/D3D12_BOX","direct3d12.d3d12_box"]
old-location: direct3d12\d3d12_box.htm
tech.root: direct3d12
ms.assetid: DD3973CC-043E-486E-9403-B46D8B7DE644
ms.date: 12/05/2018
ms.keywords: D3D12_BOX, D3D12_BOX structure, d3d12/D3D12_BOX, direct3d12.d3d12_box
req.header: d3d12.h
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
req.typenames: D3D12_BOX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_BOX
 - d3d12/D3D12_BOX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_BOX
---

# D3D12_BOX structure


## -description

Describes a 3D box.

## -struct-fields

### -field left

The x position of the left hand side of the box.

### -field top

The y position of the top of the box.

### -field front

The z position of the front of the box.

### -field right

The x position of the right hand side of the box, plus 1. This means that <code>right - left</code> equals the width of the box.

### -field bottom

The y position of the bottom of the box, plus 1. This means that <code>bottom - top</code> equals the height of the box.

### -field back

The z position of the back of the box, plus 1. This means that <code>back - front</code> equals the depth of the box.

## -remarks

This structure is used by the methods <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource">WriteToSubresource</a>, <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource">ReadFromSubresource</a> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a>.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-box">CD3DX12_BOX</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
