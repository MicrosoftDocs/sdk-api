---
UID: NS:d3d12.D3D12_DXIL_LIBRARY_DESC
title: D3D12_DXIL_LIBRARY_DESC (d3d12.h)
description: Describes a DXIL library state subobject that can be included in a state object.
helpviewer_keywords: ["D3D12_DXIL_LIBRARY_DESC","D3D12_DXIL_LIBRARY_DESC structure","PD3D12_DXIL_LIBRARY_DESC","PD3D12_DXIL_LIBRARY_DESC structure pointer","d3d12/D3D12_DXIL_LIBRARY_DESC","d3d12/PD3D12_DXIL_LIBRARY_DESC","direct3d12.d3d12_dxil_library_desc"]
old-location: direct3d12\d3d12_dxil_library_desc.htm
tech.root: direct3d12
ms.assetid: C21E91D4-C307-40D8-A82E-DDB542C1D346
ms.date: 12/05/2018
ms.keywords: D3D12_DXIL_LIBRARY_DESC, D3D12_DXIL_LIBRARY_DESC structure, PD3D12_DXIL_LIBRARY_DESC, PD3D12_DXIL_LIBRARY_DESC structure pointer, d3d12/D3D12_DXIL_LIBRARY_DESC, d3d12/PD3D12_DXIL_LIBRARY_DESC, direct3d12.d3d12_dxil_library_desc
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
req.typenames: D3D12_DXIL_LIBRARY_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DXIL_LIBRARY_DESC
 - d3d12/D3D12_DXIL_LIBRARY_DESC
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
 - D3D12_DXIL_LIBRARY_DESC
---

# D3D12_DXIL_LIBRARY_DESC structure


## -description

Describes a DXIL library state subobject that can be included in a state object.

## -struct-fields

### -field DXILLibrary

The library to include in the state object.  Must have been compiled with library target 6.3 or higher.  It is fine to specify the same library multiple times either in the same state object / collection or across multiple, as long as the names exported each time don’t conflict in a given state object.

### -field NumExports

The size of <i>pExports</i> array.  If 0, everything gets exported from the library.



#### pExports

Optional exports array.  For more information, see <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_export_desc">D3D12_EXPORT_DESC</a>.

### -field pExports