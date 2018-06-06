---
UID: NF:powrprof.WritePwrScheme
title: WritePwrScheme function
author: windows-sdk-content
description: Writes policy settings that are unique to the specified power scheme.
old-location: base\writepwrscheme.htm
old-project: Power
ms.assetid: b9233601-6848-41c4-bb58-27decad60ba5
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: WritePwrScheme, WritePwrScheme function, _win32_writepwrscheme, base.writepwrscheme, powrprof/WritePwrScheme
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
 - WritePwrScheme
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# WritePwrScheme function


## -description


<p class="CCE_Message">[<b>WritePwrScheme</b> is no longer available for use as of Windows Vista. Instead, use the <a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a> function to enumerate power settings for a specified scheme, and the power write functions to write individual settings.]

Writes policy settings that are unique to the specified power scheme.


## -parameters




### -param puiID [in]

The index of the power scheme to be written. If a power scheme with the same index already exists, it is replaced. Otherwise, a new power scheme is created.


### -param lpszSchemeName

TBD


### -param lpszDescription [in, optional]

The description of the power scheme.


### -param lpScheme

TBD




#### - lpszName [in]

The name of the power scheme.


#### - pPowerPolicy [in]

A pointer to a 
<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a> structure that contains the power policy settings to be written.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This change does not affect the current system power policy. To apply this change to the current system power policy, call the 
<a href="https://msdn.microsoft.com/f449ff0d-5c22-4c6d-8c88-dc18258a8c6d">SetActivePwrScheme</a> function with the index of this power scheme.

Power policy schemes written using 
<b>WritePwrScheme</b> are permanently stored in the system registry hives, and remain available for use in the Power Options control panel program, or by subsequent calls to the power scheme API. To permanently remove a power scheme from the system, call the 
<a href="https://msdn.microsoft.com/c9513835-00c4-4260-a8b6-d947539c9dd1">DeletePwrScheme</a> function.

For more information about using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/c9513835-00c4-4260-a8b6-d947539c9dd1">DeletePwrScheme</a>



<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>



<a href="https://msdn.microsoft.com/a8d93820-b652-4358-8039-8987fac95dca">ReadPwrScheme</a>



<a href="https://msdn.microsoft.com/f449ff0d-5c22-4c6d-8c88-dc18258a8c6d">SetActivePwrScheme</a>
 

 

