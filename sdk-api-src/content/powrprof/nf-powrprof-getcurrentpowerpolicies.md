---
UID: NF:powrprof.GetCurrentPowerPolicies
title: GetCurrentPowerPolicies function
author: windows-sdk-content
description: Retrieves the current system power policy settings.
old-location: base\getcurrentpowerpolicies.htm
old-project: Power
ms.assetid: 9a834fb6-35ae-4d36-885c-0d81cd39e9a6
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: GetCurrentPowerPolicies, GetCurrentPowerPolicies function, _win32_getcurrentpowerpolicies, base.getcurrentpowerpolicies, powrprof/GetCurrentPowerPolicies
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
 - GetCurrentPowerPolicies
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: ADAM
---

# GetCurrentPowerPolicies function


## -description


Retrieves the current system power policy settings.


## -parameters




### -param pGlobalPowerPolicy [out]

A pointer to a 
<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a> structure that receives the current global power policy settings.


### -param pPowerPolicy [out]

A pointer to a 
<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a> structure that receives the power policy settings that are unique to the active power scheme.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To update the current power policy settings, call the 
<a href="https://msdn.microsoft.com/293dc3a5-5e6b-4709-8439-67d2339740e7">WriteGlobalPwrPolicy</a> or 
<a href="https://msdn.microsoft.com/b9233601-6848-41c4-bb58-27decad60ba5">WritePwrScheme</a> functions.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>



<a href="https://msdn.microsoft.com/293dc3a5-5e6b-4709-8439-67d2339740e7">WriteGlobalPwrPolicy</a>



<a href="https://msdn.microsoft.com/b9233601-6848-41c4-bb58-27decad60ba5">WritePwrScheme</a>
 

 

