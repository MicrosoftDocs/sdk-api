---
UID: NE:sysinfoapi.DEVELOPER_DRIVE_ENABLEMENT_STATE
tech.root: winprog
title: DEVELOPER_DRIVE_ENABLEMENT_STATE (sysinfoapi.h)
ms.date: 07/31/2023
targetos: Windows
description: An enumeration of the possible values of the developer drive enablement state.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: sysinfoapi.h
req.include-header: Windows.h
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 23H2 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sysinfoapi.h
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-7.dll
api_name:
 - DEVELOPER_DRIVE_ENABLEMENT_STATE
f1_keywords:
 - DEVELOPER_DRIVE_ENABLEMENT_STATE
 - sysinfoapi/DEVELOPER_DRIVE_ENABLEMENT_STATE
dev_langs:
 - c++
helpviewer_keywords:
 - DEVELOPER_DRIVE_ENABLEMENT_STATE
---

# DEVELOPER_DRIVE_ENABLEMENT_STATE enumeration

## -description

An enum of possible values for the developer drive enablement state.

## -enum-fields

### -field DeveloperDriveEnablementStateError

Indicates that there was an error determining the developer drive enablement state. After this is returned, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the error value.

### -field DeveloperDriveEnabled

Indicates that the developer drive is enabled.

### -field DeveloperDriveDisabledBySystemPolicy

Indicates that the developer drive is disabled by system policy.

### -field DeveloperDriveDisabledByGroupPolicy

Indicates that the developer drive is disabled by group policy.

## -remarks

## -see-also

[GetDeveloperDriveEnablementState](nf-sysinfoapi-getdeveloperdriveenablementstate.md)
