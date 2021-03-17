---
UID: NF:powrprof.DevicePowerOpen
title: DevicePowerOpen function (powrprof.h)
description: Initializes a device list by querying all the devices.
helpviewer_keywords: ["DevicePowerOpen","DevicePowerOpen function","base.devicepoweropen","powrprof/DevicePowerOpen"]
old-location: base\devicepoweropen.htm
tech.root: base
ms.assetid: 1f0e8ee6-cd9e-468a-ba9a-f11e17852f89
ms.date: 12/05/2018
ms.keywords: DevicePowerOpen, DevicePowerOpen function, base.devicepoweropen, powrprof/DevicePowerOpen
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DevicePowerOpen
 - powrprof/DevicePowerOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - DevicePowerOpen
---

# DevicePowerOpen function


## -description

Initializes a device list by querying all the devices.

## -parameters

### -param DebugMask [optional]

Reserved; must be 0.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/Power/device-power-management">Device Power Management</a>