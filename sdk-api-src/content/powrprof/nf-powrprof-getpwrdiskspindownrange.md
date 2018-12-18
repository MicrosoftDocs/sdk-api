---
UID: NF:powrprof.GetPwrDiskSpindownRange
title: GetPwrDiskSpindownRange function
author: windows-sdk-content
description: Retrieves the disk spindown range.
old-location: base\getpwrdiskspindownrange.htm
tech.root: power
ms.assetid: c56f679d-512a-4bf9-89dc-8905bba8c6ce
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPwrDiskSpindownRange, GetPwrDiskSpindownRange function, _win32_getpwrdiskspindownrange, base.getpwrdiskspindownrange, powrprof/GetPwrDiskSpindownRange
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
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - GetPwrDiskSpindownRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPwrDiskSpindownRange function


## -description


<p class="CCE_Message">[<b>GetPwrDiskSpindownRange</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Retrieves the disk spindown range.


## -parameters




### -param puiMax [out]

The maximum disk spindown time, in seconds.


### -param puiMin [out]

The minimum disk spindown time, in seconds.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Starting with Windows Vista, power management configuration of the system's hard disk drives is controlled through the GUID_DISK_SUBGROUP power settings subgroup. Use the <a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a> function to enumerate individual settings.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>
 

 

