---
UID: NF:powrprof.PowerSetUserConfiguredACPowerMode
tech.root: base
title: PowerSetUserConfiguredACPowerMode function (powrprof.h)
ms.date: 02/24/2025
targetos: Windows
description: Updates the user configured power mode setting when the device is in an AC (adapter/charge) supply state.
ms.custom: 23H2
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.header: powrprof.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: powrprof.lib
req.dll: powrprof.dll
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 [desktop apps only]
req.target-min-winversvr: Windows Server 23H2 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - powrprof.h
 - api-ms-win-power-setting-l1-1-0.dll
api_name:
 - PowerSetUserConfiguredACPowerMode
f1_keywords:
 - PowerSetUserConfiguredACPowerMode
 - powrprof/PowerSetUserConfiguredACPowerMode
dev_langs:
 - c++
helpviewer_keywords:
 - PowerSetUserConfiguredACPowerMode
---

# PowerSetUserConfiguredACPowerMode function

## -description

Updates the user configured power mode setting when the device is in an AC (adapter/charge) supply state.

## -parameters

### -param PowerModeGuid [in]

A pointer to a GUID buffer that specifies the user configured power mode.

| Value                                                                        | Meaning                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **GUID_POWER_MODE_BEST_EFFICIENCY**<br>961cc777-2547-4f9d-8174-7d86181b8a7a  | Select this power mode to bias towards device energy efficiency.                     |
| **GUID_POWER_MODE_NONE**<br>00000000-0000-0000-0000-000000000000             | Select this power mode for a balance between performance and energy efficiency. |
| **GUID_POWER_MODE_BEST_PERFORMANCE**<br>ded574b5-45a0-4f42-8737-46345c09c238 | Select this power mode to bias towards device performance.                           |

## -returns

If the function succeeds, it returns **ERROR_SUCCESS**. If the function fails, it returns a system error code.

## -remarks

Windows comes installed with three default power modes that have preconfigured power setting values: "Best Power Efficiency", "Balanced", and "Best Performance". These power modes cannot be removed or changed and are the only supported values for the user configured power mode.

The user configured power mode is designed as a vote on system behavior from the user. It can be overridden by other system signals. Calling this function immediately updates the user configured power mode, while the system internals will immediately check if the effective power mode can also be updated. If there are no other signals overriding the user configured power mode, it will become the effective power mode and its setting values will be applied to the runtime system state.

> [!NOTE]
> Power modes were previously referred to as "overlays" or "overlay schemes".

## -see-also

[Power Management Functions](/windows/desktop/Power/power-management-functions)
