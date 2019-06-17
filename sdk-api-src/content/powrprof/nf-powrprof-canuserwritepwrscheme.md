---
UID: NF:powrprof.CanUserWritePwrScheme
title: CanUserWritePwrScheme function (powrprof.h)
author: windows-sdk-content
description: Determines whether the current user has sufficient privilege to write a power scheme.
old-location: base\canuserwritepwrscheme.htm
tech.root: power
ms.assetid: 3989da98-aa01-4c63-a74c-ce7ba18278c1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CanUserWritePwrScheme, CanUserWritePwrScheme function, _win32_canuserwritepwrscheme, base.canuserwritepwrscheme, powrprof/CanUserWritePwrScheme
ms.topic: function
f1_keywords: ["powrprof/CanUserWritePwrScheme"]
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
 - CanUserWritePwrScheme
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CanUserWritePwrScheme function


## -description


<p class="CCE_Message">[<b>CanUserWritePwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-powersettingaccesscheck">PowerSettingAccessCheck</a> instead.]

Determines whether the current user has sufficient privilege to write a power scheme.


## -parameters






## -returns



If the current user has sufficient privilege to write a power scheme, the function returns <b>TRUE</b>.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include the following.

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

For more information on using PowrProf.h, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-schemes">Power Schemes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-writepwrscheme">WritePwrScheme</a>
 

 

