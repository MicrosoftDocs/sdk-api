---
UID: NF:sysinfoapi.GetDeveloperDriveEnablementState
tech.root: winprog
title: GetDeveloperDriveEnablementState (sysinfoapi.h)
ms.date: 07/31/2023
targetos: Windows
description: Gets a value indicating whether the developer drive is enabled.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: api-ms-win-core-sysinfo-l1-2-6.dll
req.header: sysinfoapi.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 23H2 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sysinfoapi.h
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-7.dll
api_name:
 - GetDeveloperDriveEnablementState
f1_keywords:
 - GetDeveloperDriveEnablementState
 - sysinfoapi/GetDeveloperDriveEnablementState
dev_langs:
 - c++
helpviewer_keywords:
 - GetDeveloperDriveEnablementState
---

# GetDeveloperDriveEnablementState function

## -description

Gets a value indicating whether the developer drive is enabled.

## -returns

Returns a [DEVELOPER_DRIVE_ENABLEMENT_STATE](ne-sysinfoapi-developer_drive_enablement_state.md) value indicating the developer drive enablement state.

## -remarks

**GetDeveloperDriveEnablementState** returns information indicating whether the developer drive feature is enabled. If the developer drive feature is disabled, the **DEVELOPER_DRIVE_ENABLEMENT_STATE** returned indicates whether developer drive is disabled via group policy or via local policy.

If **GetDeveloperDriveEnablementState** fails, it returns **DeveloperDriveEnablementStateError** and sets the last error.

#### Examples

The following example shows how to use **GetDeveloperDriveEnablementState** to determine whether the developer drive is enabled.

```cpp
#include <Windows.h>

void PrintDevDriveEnabledStatus()
{
    DEVELOPER_DRIVE_ENABLEMENT_STATE state = GetDeveloperDriveEnablementState();

    switch (state) {
    case DeveloperDriveEnabled:
        printf("Developer drive is enabled.\n");
        break;
    case DeveloperDriveDisabledByGroupPolicy:
        printf("Developer drive is disabled by Group Policy.\n");
        break;
    case DeveloperDriveEnablementStateError:
        printf("Error querying developer drive info: %d\n", GetLastError());
        break;
    case DeveloperDriveDisabledBySystemPolicy:
    default:
        printf("Developer drive is disabled.");
        break;
    }
}
```

## -see-also

[DEVELOPER_DRIVE_ENABLEMENT_STATE](ne-sysinfoapi-developer_drive_enablement_state.md)
