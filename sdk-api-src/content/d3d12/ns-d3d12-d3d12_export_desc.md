---
UID: NS:d3d12.D3D12_EXPORT_DESC
title: D3D12_EXPORT_DESC (d3d12.h)
description: Describes an export from a state subobject such as a DXIL library or a collection state object.
helpviewer_keywords: ["D3D12_EXPORT_DESC","D3D12_EXPORT_DESC structure","PD3D12_EXPORT_DESC","PD3D12_EXPORT_DESC structure pointer","d3d12/D3D12_EXPORT_DESC","d3d12/PD3D12_EXPORT_DESC","direct3d12.d3d12_export_desc"]
old-location: direct3d12\d3d12_export_desc.htm
tech.root: direct3d12
ms.assetid: 15E4D40F-85E8-451E-A076-052C0C5CF304
ms.date: 12/05/2018
ms.keywords: D3D12_EXPORT_DESC, D3D12_EXPORT_DESC structure, PD3D12_EXPORT_DESC, PD3D12_EXPORT_DESC structure pointer, d3d12/D3D12_EXPORT_DESC, d3d12/PD3D12_EXPORT_DESC, direct3d12.d3d12_export_desc
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
req.typenames: D3D12_EXPORT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_EXPORT_DESC
 - d3d12/D3D12_EXPORT_DESC
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
 - D3D12_EXPORT_DESC
---

# D3D12_EXPORT_DESC structure


## -description

Describes an export from a state subobject such as a DXIL library or a collection state object.

## -struct-fields

### -field Name

The name to be exported.  If the name refers to a function that is overloaded, a modified version of the name (e.g. encoding function parameter information  in name string) can be provided to disambiguate which overload to use.  The modified name for a function can be retrieved using HLSL compiler reflection.

If the <i>ExportToRename</i> field is non-null, <i>Name</i> refers to the new name to use for it when exported.  In this case <i>Name</i> must be the unmodified name, whereas <i>ExportToRename</i> can be either a modified or unmodified name.  A given internal name may be exported multiple times with different renames (and/or not renamed).

### -field ExportToRename

If non-null, this is the name of an export to use but then rename when exported.  



#### Flags

The flags to apply to the export.

### -field Flags

