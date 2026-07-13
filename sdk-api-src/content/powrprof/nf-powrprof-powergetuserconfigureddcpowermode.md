---
UID: NF:powrprof.PowerGetUserConfiguredDCPowerMode
tech.root: base
title: PowerGetUserConfiguredDCPowerMode function (powrprof.h)
ms.date: 02/24/2025
targetos: Windows
description: Retrieves the user configured power mode GUID when the device is in an AC (adapter/charge) supply state.
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
 - PowerGetUserConfiguredDCPowerMode
f1_keywords:
 - PowerGetUserConfiguredDCPowerMode
 - powrprof/PowerGetUserConfiguredDCPowerMode
dev_langs:
 - c++
helpviewer_keywords:
 - PowerGetUserConfiguredDCPowerMode
---

# PowerGetUserConfiguredDCPowerMode function

## -description

Retrieves the user configured power mode GUID when the device is in a DC (battery/drain) supply state.

## -parameters

### -param PowerModeGuid [out]

A pointer to a GUID buffer that receives the user configured power mode GUID on a successful return.

| Value                                                                        | Meaning                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **GUID_POWER_MODE_BEST_EFFICIENCY**<br>961cc777-2547-4f9d-8174-7d86181b8a7a  | This power mode indicates the device is biased towards energy efficiency.                     |
| **GUID_POWER_MODE_NONE**<br>00000000-0000-0000-0000-000000000000             | This power mode indicates the device has a balance between performance and energy efficiency. |
| **GUID_POWER_MODE_BEST_PERFORMANCE**<br>ded574b5-45a0-4f42-8737-46345c09c238 | This power mode indicates the device is biased towards performance.                           |

## -returns

If the function succeeds, it returns **ERROR_SUCCESS**. If the function fails, it returns a system error code.

## -remarks

Windows comes installed with three default power modes that have preconfigured power setting values: "Best Power Efficiency", "Balanced", and "Best Performance". These power modes cannot be removed or changed and are the only supported values for the user configured power mode.

> [!NOTE]
> Power modes were previously referred to as "overlays" or "overlay schemes".

## -see-also

[Power Management Functions](/windows/desktop/Power/power-management-functions)
