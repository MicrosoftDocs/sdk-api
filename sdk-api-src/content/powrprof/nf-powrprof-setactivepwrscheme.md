---
UID: NF:powrprof.SetActivePwrScheme
title: SetActivePwrScheme function
author: windows-sdk-content
description: Sets the active power scheme.
old-location: base\setactivepwrscheme.htm
old-project: Power
ms.assetid: f449ff0d-5c22-4c6d-8c88-dc18258a8c6d
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: SetActivePwrScheme, SetActivePwrScheme function, _win32_setactivepwrscheme, base.setactivepwrscheme, powrprof/SetActivePwrScheme
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: powrprof.h
req.include-header: 
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
req.typenames: POWER_DATA_ACCESSOR, *PPOWER_DATA_ACCESSOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - SetActivePwrScheme
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetActivePwrScheme function


## -description


<p class="CCE_Message">[<b>SetActivePwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use 
<a href="https://msdn.microsoft.com/e56bc3f4-2141-4be7-8479-12f8d59971af">PowerSetActiveScheme</a> instead.]

Sets the active power scheme.


## -parameters




### -param uiID [in]

The index of the power scheme to be activated.


### -param pGlobalPowerPolicy

TBD


### -param pPowerPolicy

TBD




#### - lpGlobalPowerPolicy [in, optional]

A pointer to an optional 
<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a> structure, which provides global power policy settings to be merged with the power scheme when it becomes active.


#### - lpPowerPolicy [in, optional]

A pointer to an optional 
<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a> structure, which provides power policy settings to be merged with the power scheme when it becomes active.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Use this function to make long-term changes to the system configuration. To temporarily keep the system running while an application is performing a task, use the <a href="https://msdn.microsoft.com/9214ea84-7636-4a78-91fd-a5a5da8199a1">SetThreadExecutionState</a> function.

If the power scheme specified by <i>uiID</i> does not exist, the function returns zero.

If <i>lpGlobalPowerPolicy</i> is <b>NULL</b>, the function uses the current global power policy settings set by 
<a href="https://msdn.microsoft.com/293dc3a5-5e6b-4709-8439-67d2339740e7">WriteGlobalPwrPolicy</a>. Otherwise, the settings in the specified structure replace the current global power policy settings.

If <i>lpPowerPolicy</i> is <b>NULL</b>, the function uses the current power policy settings for the power scheme. Otherwise, the settings in the specified structure replace the current power policy settings.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/2a321372-40ff-4292-8b66-db3f794e5f53">GetActivePwrScheme</a>



<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>
 

 

