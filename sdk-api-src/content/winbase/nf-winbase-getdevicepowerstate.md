---
UID: NF:winbase.GetDevicePowerState
title: GetDevicePowerState function (winbase.h)
description: Retrieves the current power state of the specified device.
helpviewer_keywords: ["GetDevicePowerState","GetDevicePowerState function","_win32_getdevicepowerstate","base.getdevicepowerstate","winbase/GetDevicePowerState"]
old-location: base\getdevicepowerstate.htm
tech.root: base
ms.assetid: 017965d8-78f1-4643-b3d1-25f1303bced7
ms.date: 12/05/2018
ms.keywords: GetDevicePowerState, GetDevicePowerState function, _win32_getdevicepowerstate, base.getdevicepowerstate, winbase/GetDevicePowerState
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDevicePowerState
 - winbase/GetDevicePowerState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
api_name:
 - GetDevicePowerState
---

# GetDevicePowerState function


## -description

Retrieves the current power state of the specified device. This function cannot be used to query the power state of a display device.

## -parameters

### -param hDevice [in]

A handle to an object on the device, such as a file or socket, or a handle to the device itself.

### -param pfOn [out]

A pointer to the variable that receives the 
<a href="/windows/desktop/Power/system-power-states">power state</a>. This value is <b>TRUE</b> if the device is in the working state. Otherwise, it is <b>FALSE</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

An application can use 
<b>GetDevicePowerState</b> to determine whether a device is in the working state or a low-power state. If the device is in a low-power state, accessing the device may cause it to either queue or fail any I/O requests, or transition the device into the working state. The exact behavior depends on the implementation of the device.

To ensure maximum battery life on a laptop computer, use 
<b>GetDevicePowerState</b> to reduce power consumption. For example, if a disk is currently powered down, accessing the disk will cause it to spin up, resulting in increased power consumption and reduced battery life.

Applications should defer or limit access to devices wherever possible while the system is running on battery power. To determine whether the system is running on battery power, and the remaining battery life, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-getsystempowerstatus">GetSystemPowerStatus</a> function.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getsystempowerstatus">GetSystemPowerStatus</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/Power/system-power-status">System Power Status</a>