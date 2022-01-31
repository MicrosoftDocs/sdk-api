---
UID: NE:vss._VSS_RECOVERY_OPTIONS
title: VSS_RECOVERY_OPTIONS (vss.h)
description: Used by a requester to specify how a resynchronization operation is to be performed.
helpviewer_keywords: ["*PVSS_RECOVERY_OPTIONS","VSS_RECOVERY_NO_VOLUME_CHECK","VSS_RECOVERY_OPTIONS","VSS_RECOVERY_OPTIONS enumeration","VSS_RECOVERY_REVERT_IDENTITY_ALL","base.vss_recovery_options","vss/VSS_RECOVERY_NO_VOLUME_CHECK","vss/VSS_RECOVERY_OPTIONS","vss/VSS_RECOVERY_REVERT_IDENTITY_ALL"]
old-location: base\vss_recovery_options.htm
tech.root: base
ms.assetid: 5e58284b-9bbc-47f7-9a44-26d7153b4a25
ms.date: 12/05/2018
ms.keywords: '*PVSS_RECOVERY_OPTIONS, VSS_RECOVERY_NO_VOLUME_CHECK, VSS_RECOVERY_OPTIONS, VSS_RECOVERY_OPTIONS enumeration, VSS_RECOVERY_REVERT_IDENTITY_ALL, base.vss_recovery_options, vss/VSS_RECOVERY_NO_VOLUME_CHECK, vss/VSS_RECOVERY_OPTIONS, vss/VSS_RECOVERY_REVERT_IDENTITY_ALL'
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VSS_RECOVERY_OPTIONS, *PVSS_RECOVERY_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_RECOVERY_OPTIONS
 - vss/_VSS_RECOVERY_OPTIONS
 - PVSS_RECOVERY_OPTIONS
 - vss/PVSS_RECOVERY_OPTIONS
 - VSS_RECOVERY_OPTIONS
 - vss/VSS_RECOVERY_OPTIONS
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
 - VSS_RECOVERY_OPTIONS
---

# VSS_RECOVERY_OPTIONS enumeration


## -description

Used by a requester to specify how a resynchronization operation is to be performed.

## -enum-fields

### -field VSS_RECOVERY_REVERT_IDENTITY_ALL:0x100

 After the resynchronization operation is complete, the signature of each target LUN  should be identical to that of the original LUN that was used to create the shadow copy.

### -field VSS_RECOVERY_NO_VOLUME_CHECK:0x200

Volume safety checks should not be performed.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex3-recoverset">IVssBackupComponentsEx3::RecoverSet</a>
