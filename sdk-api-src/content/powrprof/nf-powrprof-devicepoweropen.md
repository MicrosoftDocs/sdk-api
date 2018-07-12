---
UID: NF:powrprof.DevicePowerOpen
title: DevicePowerOpen function
author: windows-sdk-content
description: Initializes a device list by querying all the devices.
old-location: base\devicepoweropen.htm
old-project: power
ms.assetid: 1f0e8ee6-cd9e-468a-ba9a-f11e17852f89
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: DevicePowerOpen, DevicePowerOpen function, base.devicepoweropen, powrprof/DevicePowerOpen
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: POWER_DATA_ACCESSOR, *PPOWER_DATA_ACCESSOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - DevicePowerOpen
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: ADAM
---

# DevicePowerOpen function


## -description


Initializes a device list by querying all the devices.


## -parameters




### -param DebugMask

TBD




#### - Flags [optional]

Reserved; must be 0.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/aaa776e5-3fc2-41bd-a805-6c09ef73807b">Device Power Management</a>
 

 

