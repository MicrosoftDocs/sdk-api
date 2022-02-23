---
UID: NE:cfapi.CF_PLACEHOLDER_MANAGEMENT_POLICY
tech.root: cloudapi
title: CF_PLACEHOLDER_MANAGEMENT_POLICY
ms.date: 02/23/2022
targetos: Windows
description: Specifies a placeholder management policy for a CF_SYNC_POLICIES structure.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: cfapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 1709
req.target-min-winversvr: Windows Server 2016
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - cfapi.h
api_name:
 - CF_PLACEHOLDER_MANAGEMENT_POLICY
f1_keywords:
 - CF_PLACEHOLDER_MANAGEMENT_POLICY
 - cfapi/CF_PLACEHOLDER_MANAGEMENT_POLICY
dev_langs:
 - c++
---

## -description

Specifies a placeholder management policy for a [CF_SYNC_POLICIES](ns-cfapi-cf_sync_policies.md) structure.

## -enum-fields

### -field CF_PLACEHOLDER_MANAGEMENT_POLICY_DEFAULT : 0x00000000
 
Only a sync provider can perform placeholder management operations in a sync roo

### -field CF_PLACEHOLDER_MANAGEMENT_POLICY_CREATE_UNRESTRICTED : 0x00000001

Any process can create a placeholder within an active sync root.

### -field CF_PLACEHOLDER_MANAGEMENT_POLICY_CONVERT_TO_UNRESTRICTED : 0x00000002

Any process can convert a file within an active sync root to a placeholder.

### -field CF_PLACEHOLDER_MANAGEMENT_POLICY_UPDATE_UNRESTRICTED : 0x00000004

Any process can update a placeholder within an active sync root.

## -remarks

By default, only a sync provider can perform placeholder management operations in a sync root. Non sync provider processes can perform placeholder management operations only if the sync root is inactive, i.e., when the sync root is not connected to by any sync provider. These policies, when enabled, allow non sync provider processes to perform respective placeholder management operations in an active sync root. The default policy allowing only a connected sync provider to perform any placeholder management operations. The three other policies can be specified in any combination.

## -see-also

[CF_SYNC_POLICIES](ns-cfapi-cf_sync_policies.md)
