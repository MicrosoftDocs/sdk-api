---
UID: NS:d3d12.D3D12_PROTECTED_RESOURCE_SESSION_DESC
title: D3D12_PROTECTED_RESOURCE_SESSION_DESC
description: Describes flags for a protected resource session, per adapter.
helpviewer_keywords: ["D3D12_PROTECTED_RESOURCE_SESSION_DESC","D3D12_PROTECTED_RESOURCE_SESSION_DESC structure","d3d12/D3D12_PROTECTED_RESOURCE_SESSION_DESC","direct3d12.d3d12_protected_resource_session_desc"]
tech.root: direct3d12
ms.date: 10/15/2019
ms.keywords: D3D12_PROTECTED_RESOURCE_SESSION_DESC, D3D12_PROTECTED_RESOURCE_SESSION_DESC structure, d3d12/D3D12_PROTECTED_RESOURCE_SESSION_DESC, direct3d12.d3d12_protected_resource_session_desc
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: D3D12_PROTECTED_RESOURCE_SESSION_DESC
req.redist: 
f1_keywords:
 - D3D12_PROTECTED_RESOURCE_SESSION_DESC
 - d3d12/D3D12_PROTECTED_RESOURCE_SESSION_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_PROTECTED_RESOURCE_SESSION_DESC
---

## -description

Describes flags for a protected resource session, per adapter.

## -struct-fields

### -field NodeMask

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The node mask. For single GPU operation, set this to zero. If there are multiple GPU nodes, then set a bit to identify the node (the device's physical adapter) to which the protected session applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Flags

Type: **[D3D12_PROTECTED_RESOURCE_SESSION_FLAGS](./ne-d3d12-d3d12_protected_resource_session_flags.md)**

Specifies the supported crypto sessions options.

## -remarks

## -see-also
