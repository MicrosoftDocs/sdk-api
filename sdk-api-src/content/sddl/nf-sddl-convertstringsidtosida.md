---
UID: NF:sddl.ConvertStringSidToSidA
title: ConvertStringSidToSidA function
author: windows-sdk-content
description: Converts a string-format security identifier (SID) into a valid, functional SID. You can use this function to retrieve a SID that the ConvertSidToStringSid function converted to string format.
old-location: security\convertstringsidtosid.htm
old-project: secauthz
ms.assetid: bf7262e3-ad2c-44c4-99cb-dcf29ad36efd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ConvertStringSidToSid, ConvertStringSidToSid function [Security], ConvertStringSidToSidA, ConvertStringSidToSidW, _win32_convertstringsidtosid, sddl/ConvertStringSidToSid, sddl/ConvertStringSidToSidA, sddl/ConvertStringSidToSidW, security.convertstringsidtosid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: sddl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ConvertStringSidToSidW (Unicode) and ConvertStringSidToSidA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SCHEDULE_HEADER, *PSCHEDULE_HEADER
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
 - ConvertStringSidToSid
 - ConvertStringSidToSidA
 - ConvertStringSidToSidW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# ConvertStringSidToSidA function


## -description


The <b>ConvertStringSidToSid</b> function converts a string-format <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) into a valid, functional SID. You can use this function to retrieve a SID that the 
<a href="https://msdn.microsoft.com/e673e727-edb1-450c-9e1a-a3dc90acc929">ConvertSidToStringSid</a> function converted to string format.


## -parameters




### -param StringSid [in]

A pointer to a null-terminated string containing the string-format SID to convert. 


The SID string can use either the standard 
							S-<i>R</i>-<i>I</i>-<i>S</i>-<i>S</i>… format for SID strings, or the SID string constant format, such as "BA" for  built-in administrators. For more information about SID string notation, see 
<a href="https://msdn.microsoft.com/528412e7-c2b6-4ddd-86de-999252972421">SID Components</a>.
					


### -param Sid [out]

A pointer to a variable that receives a pointer to the converted SID. To free the returned buffer, call the 
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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
Invalid SID.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/36140833-8e30-4c32-a88a-c10751b6c223">ConvertSecurityDescriptorToStringSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/e673e727-edb1-450c-9e1a-a3dc90acc929">ConvertSidToStringSid</a>



<a href="https://msdn.microsoft.com/c5654148-fb4c-436d-9378-a1168fc82607">ConvertStringSecurityDescriptorToSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

