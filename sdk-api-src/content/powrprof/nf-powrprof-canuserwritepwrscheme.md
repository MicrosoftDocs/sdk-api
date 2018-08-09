---
UID: NF:powrprof.CanUserWritePwrScheme
title: CanUserWritePwrScheme function
author: windows-sdk-content
description: Determines whether the current user has sufficient privilege to write a power scheme.
old-location: base\canuserwritepwrscheme.htm
old-project: power
ms.assetid: 3989da98-aa01-4c63-a74c-ce7ba18278c1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CanUserWritePwrScheme, CanUserWritePwrScheme function, _win32_canuserwritepwrscheme, base.canuserwritepwrscheme, powrprof/CanUserWritePwrScheme
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
 - CanUserWritePwrScheme
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: ADAM
---

# CanUserWritePwrScheme function


## -description


<p class="CCE_Message">[<b>CanUserWritePwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="https://msdn.microsoft.com/0b89c189-b162-44d4-aa50-d78385e40c27">PowerSettingAccessCheck</a> instead.]

Determines whether the current user has sufficient privilege to write a power scheme.


## -parameters






## -returns



If the current user has sufficient privilege to write a power scheme, the function returns <b>TRUE</b>.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Error</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The current user does not have sufficient privilege to write a power scheme.

</td>
</tr>
</table>
 




## -remarks



This function is useful if your application is impersonating a user.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>



<a href="https://msdn.microsoft.com/b9233601-6848-41c4-bb58-27decad60ba5">WritePwrScheme</a>
 

 

