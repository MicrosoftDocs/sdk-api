---
UID: NF:wldp.WldpQueryWindowsLockdownMode
tech.root: security
title: WldpQueryWindowsLockdownMode
ms.date: 08/23/2022
targetos: Windows
description: Retrieves the current Windows secure mode. Windows can be in locked mode, unlocked normal mode, or trial mode.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: wldp.dll
req.header: wldp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: wldp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: Windows Server 2016
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wldp.dll
api_name:
 - WldpQueryWindowsLockdownMode
f1_keywords:
 - WldpQueryWindowsLockdownMode
 - wldp/WldpQueryWindowsLockdownMode
dev_langs:
 - c++
helpviewer_keywords:
 - WldpQueryWindowsLockdownMode
---

## -description

Retrieves the current Windows secure mode. Windows can be in locked mode, unlocked normal mode, or trial mode.

## -parameters

### -param lockdownMode

On success, returns a [**PWLDP\_WINDOWS\_LOCKDOWN\_MODE**](ne-wldp-wldp_windows_lockdown_mode.md) that indicates the secure mode for the current Windows 10 device.

## -returns

This method returns **S\_OK** if successful or a failure code otherwise.

## -remarks

## -see-also

