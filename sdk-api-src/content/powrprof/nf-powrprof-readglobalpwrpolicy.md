---
UID: NF:powrprof.ReadGlobalPwrPolicy
title: ReadGlobalPwrPolicy function
author: windows-sdk-content
description: Retrieves the current global power policy settings.
old-location: base\readglobalpwrpolicy.htm
tech.root: power
ms.assetid: 65da3d9f-b688-4d41-9da0-05159297d169
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ReadGlobalPwrPolicy, ReadGlobalPwrPolicy function, _win32_readglobalpwrpolicy, base.readglobalpwrpolicy, powrprof/ReadGlobalPwrPolicy
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
 - ReadGlobalPwrPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReadGlobalPwrPolicy function


## -description


<p class="CCE_Message">[<b>ReadGlobalPwrPolicy</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Retrieves the current global power policy settings.


## -parameters




### -param pGlobalPowerPolicy [out]

A pointer to a 
<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a> structure that receives the information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a> structure contains policy settings that are common to all power schemes. This structure contains both user and computer policy settings.

Starting with Windows Vista, use the <a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a> function to enumerate power settings for a specified scheme and the power read functions to retrieve individual settings. 

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/293dc3a5-5e6b-4709-8439-67d2339740e7">WriteGlobalPwrPolicy</a>
 

 

