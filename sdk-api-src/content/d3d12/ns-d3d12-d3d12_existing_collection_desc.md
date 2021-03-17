---
UID: NS:d3d12.D3D12_EXISTING_COLLECTION_DESC
title: D3D12_EXISTING_COLLECTION_DESC (d3d12.h)
description: A state subobject describing an existing collection that can be included in a state object.
helpviewer_keywords: ["D3D12_EXISTING_COLLECTION_DESC","D3D12_EXISTING_COLLECTION_DESC structure","PD3D12_EXISTING_COLLECTION_DESC","PD3D12_EXISTING_COLLECTION_DESC structure pointer","d3d12/D3D12_EXISTING_COLLECTION_DESC","d3d12/PD3D12_EXISTING_COLLECTION_DESC","direct3d12.d3d12_existing_collection_desc"]
old-location: direct3d12\d3d12_existing_collection_desc.htm
tech.root: direct3d12
ms.assetid: A6E6EC48-4DCD-4D09-B110-D572B6CDE692
ms.date: 12/05/2018
ms.keywords: D3D12_EXISTING_COLLECTION_DESC, D3D12_EXISTING_COLLECTION_DESC structure, PD3D12_EXISTING_COLLECTION_DESC, PD3D12_EXISTING_COLLECTION_DESC structure pointer, d3d12/D3D12_EXISTING_COLLECTION_DESC, d3d12/PD3D12_EXISTING_COLLECTION_DESC, direct3d12.d3d12_existing_collection_desc
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
req.typenames: D3D12_EXISTING_COLLECTION_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_EXISTING_COLLECTION_DESC
 - d3d12/D3D12_EXISTING_COLLECTION_DESC
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
 - D3D12_EXISTING_COLLECTION_DESC
---

# D3D12_EXISTING_COLLECTION_DESC structure


## -description

A state subobject describing an existing collection that can be included in a state object.

## -struct-fields

### -field pExistingCollection

The collection to include in a state object.   The enclosing state object holds a reference to the existing collection.

### -field NumExports

Size of the <i>pExports</i> array.  If 0, all of the collection’s exports get exported.



#### pExports

Optional exports array.  For more information, see <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_export_desc">D3D12_EXPORT_DESC</a>.

### -field pExports