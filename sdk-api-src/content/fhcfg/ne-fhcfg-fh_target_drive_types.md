---
UID: NE:fhcfg._FH_TARGET_DRIVE_TYPES
title: FH_TARGET_DRIVE_TYPES (fhcfg.h)
description: Specifies the type of a File History backup target.
helpviewer_keywords: ["FH_DRIVE_FIXED","FH_DRIVE_REMOTE","FH_DRIVE_REMOVABLE","FH_DRIVE_UNKNOWN","FH_TARGET_DRIVE_TYPES","FH_TARGET_DRIVE_TYPES enumeration [Windows API]","fhcfg/FH_DRIVE_FIXED","fhcfg/FH_DRIVE_REMOTE","fhcfg/FH_DRIVE_REMOVABLE","fhcfg/FH_DRIVE_UNKNOWN","fhcfg/FH_TARGET_DRIVE_TYPES","winprog.fh_target_drive_types"]
old-location: winprog\fh_target_drive_types.htm
tech.root: winprog
ms.assetid: 4D3F3B57-BD6E-4334-8DF6-ECD317A051EC
ms.date: 12/05/2018
ms.keywords: FH_DRIVE_FIXED, FH_DRIVE_REMOTE, FH_DRIVE_REMOVABLE, FH_DRIVE_UNKNOWN, FH_TARGET_DRIVE_TYPES, FH_TARGET_DRIVE_TYPES enumeration [Windows API], fhcfg/FH_DRIVE_FIXED, fhcfg/FH_DRIVE_REMOTE, fhcfg/FH_DRIVE_REMOVABLE, fhcfg/FH_DRIVE_UNKNOWN, fhcfg/FH_TARGET_DRIVE_TYPES, winprog.fh_target_drive_types
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FH_TARGET_DRIVE_TYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FH_TARGET_DRIVE_TYPES
 - fhcfg/_FH_TARGET_DRIVE_TYPES
 - FH_TARGET_DRIVE_TYPES
 - fhcfg/FH_TARGET_DRIVE_TYPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fhcfg.h
api_name:
 - FH_TARGET_DRIVE_TYPES
---

# FH_TARGET_DRIVE_TYPES enumeration


## -description

Specifies the type of a File History backup target.

## -enum-fields

### -field FH_DRIVE_UNKNOWN:0

The type of the backup target is unknown.

### -field FH_DRIVE_REMOVABLE:2

The backup target is a locally attached removable storage device, such as a USB thumb drive.

### -field FH_DRIVE_FIXED:3

The backup target is a locally attached nonremovable storage device, such as an internal hard drive.

### -field FH_DRIVE_REMOTE:4

The backup target is a storage device that is accessible over network, such as a computer that is running Windows Home Server.

## -see-also

<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhtarget-getnumericalproperty">IFhTarget::GetNumericalProperty</a>
