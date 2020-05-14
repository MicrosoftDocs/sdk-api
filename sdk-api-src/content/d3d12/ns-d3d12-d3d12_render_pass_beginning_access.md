---
UID: NS:d3d12.D3D12_RENDER_PASS_BEGINNING_ACCESS
title: D3D12_RENDER_PASS_BEGINNING_ACCESS (d3d12.h)
description: Describes the access to resource(s) that is requested by an application at the transition into a render pass.helpviewer_keywords: ["D3D12_RENDER_PASS_BEGINNING_ACCESS","D3D12_RENDER_PASS_BEGINNING_ACCESS structure","d3d12/D3D12_RENDER_PASS_BEGINNING_ACCESS","direct3d12.d3d12_render_pass_beginning_access"]
old-location: direct3d12\d3d12_render_pass_beginning_access.htm
tech.root: direct3d12
ms.assetid: 48356954-F233-4FD5-A32B-099E83DC46C0
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_PASS_BEGINNING_ACCESS, D3D12_RENDER_PASS_BEGINNING_ACCESS structure, d3d12/D3D12_RENDER_PASS_BEGINNING_ACCESS, direct3d12.d3d12_render_pass_beginning_access
f1_keywords:
- d3d12/D3D12_RENDER_PASS_BEGINNING_ACCESS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- d3d12.h
api_name:
- D3D12_RENDER_PASS_BEGINNING_ACCESS
targetos: Windows
req.typenames: D3D12_RENDER_PASS_BEGINNING_ACCESS
req.redist: 
ms.custom: 19H1
---

# D3D12_RENDER_PASS_BEGINNING_ACCESS structure


## -description


Describes the access to resource(s) that is requested by an application at the transition into a render pass.


## -struct-fields




### -field Type

A <a href="https://msdn.microsoft.com/12B376DB-2CCF-493E-8B21-BAAE66B5FF1E">D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE</a>. The type of access being requested.


### -field Clear

A <a href="https://msdn.microsoft.com/E52C3630-1E57-4756-8D25-57E4A9AFDAE9">D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS</a>. Appropriate when  <b>Type</b> is <a href="https://msdn.microsoft.com/12B376DB-2CCF-493E-8B21-BAAE66B5FF1E">D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR</a>. The clear value to which resource(s) should be cleared.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/rendering">Rendering</a>
 

 

