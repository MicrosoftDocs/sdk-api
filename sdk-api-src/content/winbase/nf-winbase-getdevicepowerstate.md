---
UID: NF:winbase.GetDevicePowerState
title: GetDevicePowerState function
author: windows-sdk-content
description: Retrieves the current power state of the specified device.
old-location: base\getdevicepowerstate.htm
old-project: power
ms.assetid: 017965d8-78f1-4643-b3d1-25f1303bced7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDevicePowerState, GetDevicePowerState function, _win32_getdevicepowerstate, base.getdevicepowerstate, winbase/GetDevicePowerState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetDevicePowerState
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetDevicePowerState function


## -description


Retrieves the current power state of the specified device. This function cannot be used to query the power state of a display device.


## -parameters




### -param hDevice [in]

A handle to an object on the device, such as a file or socket, or a handle to the device itself.


### -param pfOn [out]

A pointer to the variable that receives the 
<a href="https://msdn.microsoft.com/3d897a88-125e-457f-9ea7-ac2056b0767a">power state</a>. This value is <b>TRUE</b> if the device is in the working state. Otherwise, it is <b>FALSE</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



An application can use 
<b>GetDevicePowerState</b> to determine whether a device is in the working state or a low-power state. If the device is in a low-power state, accessing the device may cause it to either queue or fail any I/O requests, or transition the device into the working state. The exact behavior depends on the implementation of the device.

To ensure maximum battery life on a laptop computer, use 
<b>GetDevicePowerState</b> to reduce power consumption. For example, if a disk is currently powered down, accessing the disk will cause it to spin up, resulting in increased power consumption and reduced battery life.

Applications should defer or limit access to devices wherever possible while the system is running on battery power. To determine whether the system is running on battery power, and the remaining battery life, use the 
<a href="https://msdn.microsoft.com/6d440ef2-2b9d-4f7a-a445-2420f07f3784">GetSystemPowerStatus</a> function.




## -see-also




<a href="https://msdn.microsoft.com/6d440ef2-2b9d-4f7a-a445-2420f07f3784">GetSystemPowerStatus</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/b9a5e7de-a603-4bd9-b854-1e58572c3b2b">System Power Status</a>
 

 

