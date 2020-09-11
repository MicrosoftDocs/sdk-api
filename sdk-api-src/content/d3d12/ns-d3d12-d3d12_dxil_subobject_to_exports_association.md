---
UID: NS:d3d12.D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
title: D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION (d3d12.h)
description: This subobject is unsupported in the current release.
helpviewer_keywords: ["D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION","D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION structure","PD3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION","PD3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION structure pointer","d3d12/D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION","d3d12/PD3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION","direct3d12.d3d12_dxil_subobject_to_exports_association"]
old-location: direct3d12\d3d12_dxil_subobject_to_exports_association.htm
tech.root: direct3d12
ms.assetid: 82990FE6-43A8-4597-BAC5-E995B1FA67EB
ms.date: 12/05/2018
ms.keywords: D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION, D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION structure, PD3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION, PD3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION structure pointer, d3d12/D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION, d3d12/PD3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION, direct3d12.d3d12_dxil_subobject_to_exports_association
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
req.typenames: D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
 - d3d12/D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
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
 - D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
---

## -description

This subobject is unsupported in the current release.

## -struct-fields

### -field SubobjectToAssociate

### -field NumExports

Size of the <i>pExports</i> array.  If 0, this is being explicitly defined as a default association.  Another way to define a default association is to omit this subobject association for that subobject completely.

### -field pExports

The array of exports with which the subobject is associated.

