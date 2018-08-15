---
UID: NF:powrprof.GetActivePwrScheme
title: GetActivePwrScheme function
author: windows-sdk-content
description: Retrieves the index of the active power scheme.
old-location: base\getactivepwrscheme.htm
old-project: power
ms.assetid: 2a321372-40ff-4292-8b66-db3f794e5f53
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetActivePwrScheme, GetActivePwrScheme function, _win32_getactivepwrscheme, base.getactivepwrscheme, powrprof/GetActivePwrScheme
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: powrprof.h
req.include-header: 
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
req.typenames: POWER_DATA_ACCESSOR, *PPOWER_DATA_ACCESSOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - GetActivePwrScheme
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: ADAM
---

# GetActivePwrScheme function


## -description


<p class="CCE_Message">[<b>GetActivePwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="https://msdn.microsoft.com/cd72562c-8987-40c1-89c7-04a95b5f1fd0">PowerGetActiveScheme</a> instead.]

Retrieves the index of the active power scheme.


## -parameters




### -param puiID [out]

A pointer to a variable that receives the index of the active power scheme.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The active power scheme remains active until either the user sets a new power scheme using the Power Options control panel program, or an application calls the 
<a href="https://msdn.microsoft.com/f449ff0d-5c22-4c6d-8c88-dc18258a8c6d">SetActivePwrScheme</a> function.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>



<a href="https://msdn.microsoft.com/f449ff0d-5c22-4c6d-8c88-dc18258a8c6d">SetActivePwrScheme</a>
 

 

