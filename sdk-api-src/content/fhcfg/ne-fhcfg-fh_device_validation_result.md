---
UID: NE:fhcfg._FH_DEVICE_VALIDATION_RESULT
title: FH_DEVICE_VALIDATION_RESULT (fhcfg.h)
description: Indicates whether the storage device or network share can be used as a File History backup target.
helpviewer_keywords: ["*PFH_DEVICE_VALIDATION_RESULT","FH_ACCESS_DENIED","FH_CURRENT_DEFAULT","FH_DEVICE_VALIDATION_RESULT","FH_DEVICE_VALIDATION_RESULT enumeration [Windows API]","FH_INVALID_DRIVE_TYPE","FH_NAMESPACE_EXISTS","FH_READ_ONLY_PERMISSION","FH_TARGET_PART_OF_LIBRARY","FH_VALID_TARGET","MAX_VALIDATION_RESULT","fhcfg/FH_ACCESS_DENIED","fhcfg/FH_CURRENT_DEFAULT","fhcfg/FH_DEVICE_VALIDATION_RESULT","fhcfg/FH_INVALID_DRIVE_TYPE","fhcfg/FH_NAMESPACE_EXISTS","fhcfg/FH_READ_ONLY_PERMISSION","fhcfg/FH_TARGET_PART_OF_LIBRARY","fhcfg/FH_VALID_TARGET","fhcfg/MAX_VALIDATION_RESULT","winprog.fh_device_validation_result"]
old-location: winprog\fh_device_validation_result.htm
tech.root: winprog
ms.assetid: DAADC244-D0F5-44F9-9F61-48E6C6EFB91A
ms.date: 12/05/2018
ms.keywords: '*PFH_DEVICE_VALIDATION_RESULT, FH_ACCESS_DENIED, FH_CURRENT_DEFAULT, FH_DEVICE_VALIDATION_RESULT, FH_DEVICE_VALIDATION_RESULT enumeration [Windows API], FH_INVALID_DRIVE_TYPE, FH_NAMESPACE_EXISTS, FH_READ_ONLY_PERMISSION, FH_TARGET_PART_OF_LIBRARY, FH_VALID_TARGET, MAX_VALIDATION_RESULT, fhcfg/FH_ACCESS_DENIED, fhcfg/FH_CURRENT_DEFAULT, fhcfg/FH_DEVICE_VALIDATION_RESULT, fhcfg/FH_INVALID_DRIVE_TYPE, fhcfg/FH_NAMESPACE_EXISTS, fhcfg/FH_READ_ONLY_PERMISSION, fhcfg/FH_TARGET_PART_OF_LIBRARY, fhcfg/FH_VALID_TARGET, fhcfg/MAX_VALIDATION_RESULT, winprog.fh_device_validation_result'
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
req.typenames: FH_DEVICE_VALIDATION_RESULT, *PFH_DEVICE_VALIDATION_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FH_DEVICE_VALIDATION_RESULT
 - fhcfg/_FH_DEVICE_VALIDATION_RESULT
 - PFH_DEVICE_VALIDATION_RESULT
 - fhcfg/PFH_DEVICE_VALIDATION_RESULT
 - FH_DEVICE_VALIDATION_RESULT
 - fhcfg/FH_DEVICE_VALIDATION_RESULT
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
 - FH_DEVICE_VALIDATION_RESULT
---

# FH_DEVICE_VALIDATION_RESULT enumeration


## -description

Indicates whether the  storage device or network share can be used as a File History backup target.

## -enum-fields

### -field FH_ACCESS_DENIED:0

The storage device or network share cannot be used as a backup target, because it is not accessible.

### -field FH_INVALID_DRIVE_TYPE

The storage device or network share cannot be used as a backup target, because the drive type is not supported.  For example, a CD or DVD cannot be used as a  File History backup target.

### -field FH_READ_ONLY_PERMISSION

The storage device or network share cannot be used as a backup target, because it is read-only.

### -field FH_CURRENT_DEFAULT

The storage device or network share is already being used as a backup target.

### -field FH_NAMESPACE_EXISTS

The storage device or network share was previously used to back up files from a computer or user that has the same name as the current computer or user. It can be used as a backup target, but if it is used, the operating system will delete the previous backup.

### -field FH_TARGET_PART_OF_LIBRARY

The storage device or network share cannot be used as a backup target, because it is in the File History protection scope.

### -field FH_VALID_TARGET

The storage device or network share can be used as a backup target.

### -field MAX_VALIDATION_RESULT

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.

## -see-also

<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-validatetarget">IFhConfigMgr::ValidateTarget</a>
