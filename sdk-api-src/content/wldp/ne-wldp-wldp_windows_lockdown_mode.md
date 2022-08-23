---
UID: NE:wldp.WLDP_WINDOWS_LOCKDOWN_MODE
tech.root: security
title: WLDP_WINDOWS_LOCKDOWN_MODE
ms.date: 08/23/2022
targetos: Windows
description: Describes the secure modes (S modes) for a Windows device.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wldp.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wldp.h
api_name:
 - WLDP_WINDOWS_LOCKDOWN_MODE
 - PWLDP_WINDOWS_LOCKDOWN_MODE
f1_keywords:
 - WLDP_WINDOWS_LOCKDOWN_MODE
 - wldp/WLDP_WINDOWS_LOCKDOWN_MODE
 - PWLDP_WINDOWS_LOCKDOWN_MODE
 - wldp/PWLDP_WINDOWS_LOCKDOWN_MODE
dev_langs:
 - c++
helpviewer_keywords:
 - WLDP_WINDOWS_LOCKDOWN_MODE
---

## -description

Describes the secure modes (S modes) for a Windows device. Used primarily in [**WldpQueryWindowsLockdownMode**](nf-wldp-wldpquerywindowslockdownmode.md).

## -enum-fields

### -field WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED

Unlocked. Used primarily for Windows devices without the S mode.

### -field WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL

Trial. Used primarily for a Windows 10 trial device with the S mode. Trial mode is a special case for Windows 10 devices with the S mode: policies are enforced, but there is no anti-rollback protection for the enforcement of the policy.

### -field WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED

Locked. Used primarily for a Windows 10 device with the S mode. A device that is locked will enforce the signed Device Guard policies shipped with the Windows 10 OS image with the S mode.

### -field WLDP_WINDOWS_LOCKDOWN_MODE_MAX

The maximum enumeration value.

## -remarks

## -see-also

