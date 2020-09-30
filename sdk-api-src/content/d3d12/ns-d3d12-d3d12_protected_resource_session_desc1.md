---
UID: NS:d3d12.D3D12_PROTECTED_RESOURCE_SESSION_DESC1
title: D3D12_PROTECTED_RESOURCE_SESSION_DESC1
description: Describes flags and protection type for a protected resource session, per adapter.
helpviewer_keywords: ["D3D12_PROTECTED_RESOURCE_SESSION_DESC1","D3D12_PROTECTED_RESOURCE_SESSION_DESC1 structure","d3d12/D3D12_PROTECTED_RESOURCE_SESSION_DESC1","direct3d12.d3d12_protected_resource_session_desc1"]
tech.root: direct3d12
ms.date: 09/16/2020
targetos: Windows
description: 
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12_PROTECTED_RESOURCE_SESSION_DESC1
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_PROTECTED_RESOURCE_SESSION_DESC1
 - d3d12/D3D12_PROTECTED_RESOURCE_SESSION_DESC1
f1_keywords:
 - d3d12/D3D12_PROTECTED_RESOURCE_SESSION_DESC1
dev_langs:
 - c++
---

## -description

Describes flags and protection type for a protected resource session, per adapter.

## -struct-fields

### -field NodeMask

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The node mask. For single GPU operation, set this to zero. If there are multiple GPU nodes, then set a bit to identify the node (the device's physical adapter) to which the protected session applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Flags

Type: **[D3D12_PROTECTED_RESOURCE_SESSION_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags)**

Specifies the supported crypto sessions options.

### -field ProtectionType

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

The GUID that represents the protection type. Microsoft defines **D3D12_PROTECTED_RESOURCES_SESSION_HARDWARE_PROTECTED**.

Using the **D3D12_PROTECTED_RESOURCES_SESSION_HARDWARE_PROTECTED** GUID is equivalent to calling [**ID3D12Device4::CreateProtectedResourceSession**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createprotectedresourcesession).

## -remarks

## -see-also
