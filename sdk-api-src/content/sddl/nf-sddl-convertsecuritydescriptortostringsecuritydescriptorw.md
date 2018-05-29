---
UID: NF:sddl.ConvertSecurityDescriptorToStringSecurityDescriptorW
title: ConvertSecurityDescriptorToStringSecurityDescriptorW function
author: windows-sdk-content
description: Converts a security descriptor to a string format. You can use the string format to store or transmit the security descriptor.
old-location: security\convertsecuritydescriptortostringsecuritydescriptor.htm
old-project: SecAuthZ
ms.assetid: 36140833-8e30-4c32-a88a-c10751b6c223
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ConvertSecurityDescriptorToStringSecurityDescriptor, ConvertSecurityDescriptorToStringSecurityDescriptor function [Security], ConvertSecurityDescriptorToStringSecurityDescriptorA, ConvertSecurityDescriptorToStringSecurityDescriptorW, _win32_convertsecuritydescriptortostringsecuritydescriptor, sddl/ConvertSecurityDescriptorToStringSecurityDescriptor, sddl/ConvertSecurityDescriptorToStringSecurityDescriptorA, sddl/ConvertSecurityDescriptorToStringSecurityDescriptorW, security.convertsecuritydescriptortostringsecuritydescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: sddl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ConvertSecurityDescriptorToStringSecurityDescriptorW (Unicode) and ConvertSecurityDescriptorToStringSecurityDescriptorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SCHEDULE_HEADER, *PSCHEDULE_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
-	sechost.dll
-	API-MS-Win-Security-sddl-l1-1-0.dll
api_name:
-	ConvertSecurityDescriptorToStringSecurityDescriptor
-	ConvertSecurityDescriptorToStringSecurityDescriptorA
-	ConvertSecurityDescriptorToStringSecurityDescriptorW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ConvertSecurityDescriptorToStringSecurityDescriptorW function


## -description


The <b>ConvertSecurityDescriptorToStringSecurityDescriptor</b> function converts a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> to a string format. You can use the string format to store or transmit the security descriptor.

To convert the string-format security descriptor back to a valid, functional security descriptor, call the 
<a href="https://msdn.microsoft.com/c5654148-fb4c-436d-9378-a1168fc82607">ConvertStringSecurityDescriptorToSecurityDescriptor</a> function.


## -parameters




### -param SecurityDescriptor [in]

A pointer to the security descriptor to convert. The security descriptor can be in 
<a href="https://msdn.microsoft.com/dab2844b-7df9-446c-aacf-380a0a805cbc">absolute or self-relative format</a>.


### -param RequestedStringSDRevision [in]

Specifies the revision level of the output <i>StringSecurityDescriptor</i> string. Currently this value must be SDDL_REVISION_1.


### -param SecurityInformation [in]

Specifies a combination of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> bit flags to indicate the components of the security descriptor to include in the output string. 




					The BACKUP_SECURITY_INFORMATION 	flag is not applicable to this function. If the BACKUP_SECURITY_INFORMATION 	flag is passed in, the <i>SecurityInformation</i> parameter returns TRUE with <b>null</b> string output.


### -param StringSecurityDescriptor [out]

A pointer to a variable that receives a pointer to a <b>null</b>-terminated security descriptor string. For a description of the string format, see 
<a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor String Format</a>. To free the returned buffer, call the 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


### -param StringSecurityDescriptorLen [out]

A pointer to a variable that receives the size, in <b>TCHAR</b>s, of the security descriptor string returned in the <i>StringSecurityDescriptor</i> buffer. This parameter can be <b>NULL</b> if you do not need to retrieve the size.


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
A parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_REVISION</b></dt>
</dl>
</td>
<td width="60%">
The revision level is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NONE_MAPPED</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in the input security descriptor could not be found in an account lookup operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ACL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) is not valid. This error is returned if the SE_DACL_PRESENT flag is set in the input security descriptor and the DACL is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



If the DACL is <b>NULL</b>, and the SE_DACL_PRESENT control bit is set in the input security descriptor, the function fails.

If the DACL is <b>NULL</b>, and the SE_DACL_PRESENT control bit is not set in the input security descriptor, the resulting security descriptor string does not have a D: component. For more information, see 
<a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor String Format</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/e673e727-edb1-450c-9e1a-a3dc90acc929">ConvertSidToStringSid</a>



<a href="https://msdn.microsoft.com/c5654148-fb4c-436d-9378-a1168fc82607">ConvertStringSecurityDescriptorToSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/bf7262e3-ad2c-44c4-99cb-dcf29ad36efd">ConvertStringSidToSid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>
 

 

