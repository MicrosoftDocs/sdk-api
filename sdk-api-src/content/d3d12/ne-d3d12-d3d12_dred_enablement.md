---
UID: NE:d3d12.D3D12_DRED_ENABLEMENT
title: D3D12_DRED_ENABLEMENT
description: Defines constants that specify render/compute GPU operations. (D3D12_DRED_ENABLEMENT)
tech.root: direct3d12
helpviewer_keywords: ["D3D12_DRED_ENABLEMENT","D3D12_DRED_ENABLEMENT enumeration","d3d12/D3D12_DRED_ENABLEMENT","d3d12/D3D12_DRED_ENABLEMENT enumeration","direct3d12.d3d12_dred_enablement"]
ms.date: 02/07/2019
ms.keywords: D3D12_DRED_ENABLEMENT, D3D12_DRED_ENABLEMENT enumeration, d3d12/D3D12_DRED_ENABLEMENT, d3d12/D3D12_DRED_ENABLEMENT enumeration, direct3d12.d3d12_dred_enablement
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D12_DRED_ENABLEMENT
req.umdf-ver: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DRED_ENABLEMENT
 - d3d12/D3D12_DRED_ENABLEMENT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_DRED_ENABLEMENT
---

# D3D12_DRED_ENABLEMENT enumeration


## -description

Defines constants (used by the [ID3D12DeviceRemovedExtendedDataSettings interface](nn-d3d12-id3d12deviceremovedextendeddatasettings.md)) that specify how individual Device Removed Extended Data (DRED) features are enabled. As of DRED version 1.1, the default value for all settings is **D3D12_DRED_ENABLEMENT_SYSTEM_CONTROLLED**.

## -enum-fields

### -field D3D12_DRED_ENABLEMENT_SYSTEM_CONTROLLED (0)

Specifies that a DRED feature is enabled only when DRED is turned on by the system automatically (for example, when a user is reproducing a problem via FeedbackHub).

### -field D3D12_DRED_ENABLEMENT_FORCED_OFF (1)

Specifies that a DRED feature should be force-disabled, regardless of the system state.

### -field D3D12_DRED_ENABLEMENT_FORCED_ON (2)

Specifies that a DRED feature should be force-enabled, regardless of the system state.

## -remarks

## -see-also

* [Core enumerations](/windows/desktop/direct3d12/direct3d-12-enumerations)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

