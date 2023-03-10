---
UID: NE:vss._VSS_HARDWARE_OPTIONS
title: VSS_HARDWARE_OPTIONS (vss.h)
description: Defines shadow copy LUN flags.
helpviewer_keywords: ["*PVSS_HARDWARE_OPTIONS","PVSS_HARDWARE_OPTIONS","PVSS_HARDWARE_OPTIONS enumeration pointer","VSS_BREAKEX_FLAG_MAKE_READ_WRITE","VSS_BREAKEX_FLAG_MASK_LUNS","VSS_BREAKEX_FLAG_REVERT_IDENTITY_ALL","VSS_BREAKEX_FLAG_REVERT_IDENTITY_NONE","VSS_HARDWARE_OPTIONS","VSS_HARDWARE_OPTIONS enumeration","VSS_ONLUNSTATECHANGE_DO_MASK_LUNS","VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY","VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY","VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE","_VSS_HARDWARE_OPTIONS","_VSS_HARDWARE_OPTIONS enumeration","base._vss_hardware_options","vss/PVSS_HARDWARE_OPTIONS","vss/VSS_BREAKEX_FLAG_MAKE_READ_WRITE","vss/VSS_BREAKEX_FLAG_MASK_LUNS","vss/VSS_BREAKEX_FLAG_REVERT_IDENTITY_ALL","vss/VSS_BREAKEX_FLAG_REVERT_IDENTITY_NONE","vss/VSS_ONLUNSTATECHANGE_DO_MASK_LUNS","vss/VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY","vss/VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY","vss/VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE","vss/_VSS_HARDWARE_OPTIONS"]
old-location: base\_vss_hardware_options.htm
tech.root: base
ms.assetid: 545977ae-7f62-4a8e-9d2f-936224f413b7
ms.date: 12/05/2018
ms.keywords: '*PVSS_HARDWARE_OPTIONS, PVSS_HARDWARE_OPTIONS, PVSS_HARDWARE_OPTIONS enumeration pointer, VSS_BREAKEX_FLAG_MAKE_READ_WRITE, VSS_BREAKEX_FLAG_MASK_LUNS, VSS_BREAKEX_FLAG_REVERT_IDENTITY_ALL, VSS_BREAKEX_FLAG_REVERT_IDENTITY_NONE, VSS_HARDWARE_OPTIONS, VSS_HARDWARE_OPTIONS enumeration, VSS_ONLUNSTATECHANGE_DO_MASK_LUNS, VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY, VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY, VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE, _VSS_HARDWARE_OPTIONS, _VSS_HARDWARE_OPTIONS enumeration, base._vss_hardware_options, vss/PVSS_HARDWARE_OPTIONS, vss/VSS_BREAKEX_FLAG_MAKE_READ_WRITE, vss/VSS_BREAKEX_FLAG_MASK_LUNS, vss/VSS_BREAKEX_FLAG_REVERT_IDENTITY_ALL, vss/VSS_BREAKEX_FLAG_REVERT_IDENTITY_NONE, vss/VSS_ONLUNSTATECHANGE_DO_MASK_LUNS, vss/VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY, vss/VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY, vss/VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE, vss/_VSS_HARDWARE_OPTIONS'
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: VSS_HARDWARE_OPTIONS, *PVSS_HARDWARE_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_HARDWARE_OPTIONS
 - vss/_VSS_HARDWARE_OPTIONS
 - PVSS_HARDWARE_OPTIONS
 - vss/PVSS_HARDWARE_OPTIONS
 - VSS_HARDWARE_OPTIONS
 - vss/VSS_HARDWARE_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_HARDWARE_OPTIONS
---

# VSS_HARDWARE_OPTIONS enumeration


## -description

Defines shadow copy LUN flags.

## -enum-fields

### -field VSS_BREAKEX_FLAG_MASK_LUNS:0x1

The shadow copy LUN will be masked from the host.

### -field VSS_BREAKEX_FLAG_MAKE_READ_WRITE:0x2

The shadow copy LUN will be exposed to the host as a read-write volume.

### -field VSS_BREAKEX_FLAG_REVERT_IDENTITY_ALL:0x4

The disk identifiers of all of the shadow copy LUNs will be reverted to that of the original LUNs. However, if any of the original LUNs are present on the system, the operation will fail and none of the identifiers will be reverted.

### -field VSS_BREAKEX_FLAG_REVERT_IDENTITY_NONE:0x8

None of the disk identifiers of the shadow copy LUNs will be reverted.

### -field VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE:0x100

The shadow copy LUNs will be converted permanently to read-write. This flag is set only as a notification for the provider; no provider action is required. For more information, see the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotproviderex-onlunstatechange">IVssHardwareSnapshotProviderEx::OnLunStateChange</a> method.

### -field VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY:0x200

The shadow copy LUNs will be converted temporarily to read-write and are about to undergo TxF recovery or VSS auto-recovery. This flag is set only as a notification for the provider; no provider action is required. For more information, see the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotproviderex-onlunstatechange">IVssHardwareSnapshotProviderEx::OnLunStateChange</a> method.

### -field VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY:0x400

The shadow copy LUNs have just undergone TxF recovery or VSS auto-recovery and have been converted back to read-only. This flag is set only as a notification for the provider; no provider action is required. For more information, see the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotproviderex-onlunstatechange">IVssHardwareSnapshotProviderEx::OnLunStateChange</a> method.

### -field VSS_ONLUNSTATECHANGE_DO_MASK_LUNS:0x800

The provider must mask shadow copy LUNs from this computer. For more information, see the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotproviderex-onlunstatechange">IVssHardwareSnapshotProviderEx::OnLunStateChange</a> method.

## -see-also

<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotproviderex-onlunstatechange">IVssHardwareSnapshotProviderEx::OnLunStateChange</a>
