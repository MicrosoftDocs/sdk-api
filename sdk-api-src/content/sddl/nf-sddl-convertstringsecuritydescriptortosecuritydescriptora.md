---
UID: NF:sddl.ConvertStringSecurityDescriptorToSecurityDescriptorA
title: ConvertStringSecurityDescriptorToSecurityDescriptorA function
author: windows-sdk-content
description: Converts a string-format security descriptor into a valid, functional security descriptor.
old-location: security\convertstringsecuritydescriptortosecuritydescriptor.htm
tech.root: secauthz
ms.assetid: c5654148-fb4c-436d-9378-a1168fc82607
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ConvertStringSecurityDescriptorToSecurityDescriptor, ConvertStringSecurityDescriptorToSecurityDescriptor function [Security], ConvertStringSecurityDescriptorToSecurityDescriptorA, ConvertStringSecurityDescriptorToSecurityDescriptorW, _win32_convertstringsecuritydescriptortosecuritydescriptor, sddl/ConvertStringSecurityDescriptorToSecurityDescriptor, sddl/ConvertStringSecurityDescriptorToSecurityDescriptorA, sddl/ConvertStringSecurityDescriptorToSecurityDescriptorW, security.convertstringsecuritydescriptortosecuritydescriptor
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
req.unicode-ansi: ConvertStringSecurityDescriptorToSecurityDescriptorW (Unicode) and ConvertStringSecurityDescriptorToSecurityDescriptorA (ANSI)
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
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Security-sddl-l1-1-0.dll
api_name:
 - ConvertStringSecurityDescriptorToSecurityDescriptor
 - ConvertStringSecurityDescriptorToSecurityDescriptorA
 - ConvertStringSecurityDescriptorToSecurityDescriptorW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ConvertStringSecurityDescriptorToSecurityDescriptorA function


## -description


The <b>ConvertStringSecurityDescriptorToSecurityDescriptor</b> function converts a string-format <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> into a valid, functional security descriptor. This function retrieves a security descriptor that the 
<a href="https://msdn.microsoft.com/36140833-8e30-4c32-a88a-c10751b6c223">ConvertSecurityDescriptorToStringSecurityDescriptor</a> function converted to string format.
		


## -parameters




### -param StringSecurityDescriptor [in]

A pointer to a null-terminated string containing the 
<a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">string-format security descriptor</a> to convert.


### -param StringSDRevision [in]

Specifies the revision level of the <i>StringSecurityDescriptor</i> string. Currently this value must be SDDL_REVISION_1.


### -param SecurityDescriptor [out]

A pointer to a variable that receives a pointer to the converted security descriptor. The returned security descriptor is <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative</a>. To free the returned buffer, call the 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function. To convert the security descriptor to an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">absolute security descriptor</a>, use the 
<a href="https://msdn.microsoft.com/47c75071-f10d-43cf-a841-2dd49fc39afa">MakeAbsoluteSD</a> function.


### -param SecurityDescriptorSize [out]

A pointer to a variable that receives the size, in bytes, of the converted security descriptor. This parameter can be NULL.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. <b>GetLastError</b> may return one of the following error codes.

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
The SDDL revision level is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NONE_MAPPED</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in the input security descriptor string could not be found in an account lookup operation.

</td>
</tr>
</table>
 




## -remarks



If <b>ace_type</b> is ACCESS_ALLOWED_OBJECT_ACE_TYPE
and neither <b>object_guid</b> nor <b>inherit_object_guid</b> has a  <a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> specified, then <b>ConvertStringSecurityDescriptorToSecurityDescriptor</b> converts <b>ace_type</b> to ACCESS_ALLOWED_ACE_TYPE. For information about the  <b>ace_type</b>,  <b>object_guid</b>, and <b>inherit_object_guid</b> fields, see <a href="https://msdn.microsoft.com/82c99170-784b-4724-a25b-2f2e8a2e0225">Ace Strings</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/36140833-8e30-4c32-a88a-c10751b6c223">ConvertSecurityDescriptorToStringSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/e673e727-edb1-450c-9e1a-a3dc90acc929">ConvertSidToStringSid</a>



<a href="https://msdn.microsoft.com/bf7262e3-ad2c-44c4-99cb-dcf29ad36efd">ConvertStringSidToSid</a>



<a href="https://msdn.microsoft.com/47c75071-f10d-43cf-a841-2dd49fc39afa">MakeAbsoluteSD</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>
 

 

