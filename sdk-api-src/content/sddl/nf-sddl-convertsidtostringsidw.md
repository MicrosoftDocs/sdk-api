---
UID: NF:sddl.ConvertSidToStringSidW
title: ConvertSidToStringSidW function
author: windows-sdk-content
description: Converts a security identifier (SID) to a string format suitable for display, storage, or transmission.
old-location: security\convertsidtostringsid.htm
tech.root: secauthz
ms.assetid: e673e727-edb1-450c-9e1a-a3dc90acc929
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ConvertSidToStringSid, ConvertSidToStringSid function [Security], ConvertSidToStringSidA, ConvertSidToStringSidW, _win32_convertsidtostringsid, sddl/ConvertSidToStringSid, sddl/ConvertSidToStringSidA, sddl/ConvertSidToStringSidW, security.convertsidtostringsid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sddl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ConvertSidToStringSidW (Unicode) and ConvertSidToStringSidA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-security-sddl-ansi-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Security-sddl-l1-1-0.dll
api_name:
 - ConvertSidToStringSid
 - ConvertSidToStringSidA
 - ConvertSidToStringSidW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ConvertSidToStringSidW function


## -description


The <b>ConvertSidToStringSid</b> function converts a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) to a string format suitable for display, storage, or transmission.

To convert the string-format SID back to a valid, functional SID, call the 
<a href="https://msdn.microsoft.com/bf7262e3-ad2c-44c4-99cb-dcf29ad36efd">ConvertStringSidToSid</a> function.


## -parameters




### -param Sid [in]

A pointer to the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure to be converted.


### -param StringSid [out]

A pointer to a variable that receives a pointer to a null-terminated SID string. To free the returned buffer, call the 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The <b>GetLastError</b> function may return one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
The SID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid. This is most often a pointer that is not valid.

</td>
</tr>
</table>
 




## -remarks



The <b>ConvertSidToStringSid</b> function uses the standard S-<i>R</i>-<i>I</i>-<i>S</i>-<i>S</i>… format for SID strings. For more information about SID string notation, see 
<a href="https://msdn.microsoft.com/528412e7-c2b6-4ddd-86de-999252972421">SID Components</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/36140833-8e30-4c32-a88a-c10751b6c223">ConvertSecurityDescriptorToStringSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/c5654148-fb4c-436d-9378-a1168fc82607">ConvertStringSecurityDescriptorToSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/bf7262e3-ad2c-44c4-99cb-dcf29ad36efd">ConvertStringSidToSid</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>
 

 

