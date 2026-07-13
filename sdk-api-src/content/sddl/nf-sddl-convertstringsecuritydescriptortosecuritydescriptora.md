---
UID: NF:sddl.ConvertStringSecurityDescriptorToSecurityDescriptorA
title: ConvertStringSecurityDescriptorToSecurityDescriptorA function (sddl.h)
description: Converts a string-format security descriptor into a valid, functional security descriptor. (ANSI)
helpviewer_keywords: ["ConvertStringSecurityDescriptorToSecurityDescriptorA", "sddl/ConvertStringSecurityDescriptorToSecurityDescriptorA"]
old-location: security\convertstringsecuritydescriptortosecuritydescriptor.htm
tech.root: security
ms.assetid: c5654148-fb4c-436d-9378-a1168fc82607
ms.date: 12/05/2018
ms.keywords: ConvertStringSecurityDescriptorToSecurityDescriptor, ConvertStringSecurityDescriptorToSecurityDescriptor function [Security], ConvertStringSecurityDescriptorToSecurityDescriptorA, ConvertStringSecurityDescriptorToSecurityDescriptorW, _win32_convertstringsecuritydescriptortosecuritydescriptor, sddl/ConvertStringSecurityDescriptorToSecurityDescriptor, sddl/ConvertStringSecurityDescriptorToSecurityDescriptorA, sddl/ConvertStringSecurityDescriptorToSecurityDescriptorW, security.convertstringsecuritydescriptortosecuritydescriptor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ConvertStringSecurityDescriptorToSecurityDescriptorA
 - sddl/ConvertStringSecurityDescriptorToSecurityDescriptorA
dev_langs:
 - c++
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
---

# ConvertStringSecurityDescriptorToSecurityDescriptorA function


## -description

The <b>ConvertStringSecurityDescriptorToSecurityDescriptor</b> function converts a string-format <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> into a valid, functional security descriptor. This function retrieves a security descriptor that the 
<a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a> function converted to string format.

## -parameters

### -param StringSecurityDescriptor [in]

A pointer to a null-terminated string containing the 
<a href="/windows/desktop/SecAuthZ/security-descriptor-string-format">string-format security descriptor</a> to convert.

### -param StringSDRevision [in]

Specifies the revision level of the <i>StringSecurityDescriptor</i> string. Currently this value must be SDDL_REVISION_1.

### -param SecurityDescriptor [out]

A pointer to a variable that receives a pointer to the converted security descriptor. The returned security descriptor is <a href="/windows/desktop/SecGloss/s-gly">self-relative</a>. To free the returned buffer, call the 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function. To convert the security descriptor to an <a href="/windows/desktop/SecGloss/a-gly">absolute security descriptor</a>, use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd">MakeAbsoluteSD</a> function.

### -param SecurityDescriptorSize [out]

A pointer to a variable that receives the size, in bytes, of the converted security descriptor. This parameter can be NULL.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>GetLastError</b> may return one of the following error codes.

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
A <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in the input security descriptor string could not be found in an account lookup operation.

</td>
</tr>
</table>

## -remarks

If <b>ace_type</b> is ACCESS_ALLOWED_OBJECT_ACE_TYPE
and neither <b>object_guid</b> nor <b>inherit_object_guid</b> has a  <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> specified, then <b>ConvertStringSecurityDescriptorToSecurityDescriptor</b> converts <b>ace_type</b> to ACCESS_ALLOWED_ACE_TYPE. For information about the  <b>ace_type</b>,  <b>object_guid</b>, and <b>inherit_object_guid</b> fields, see <a href="/windows/desktop/SecAuthZ/ace-strings">Ace Strings</a>.





> [!NOTE]
> The sddl.h header defines ConvertStringSecurityDescriptorToSecurityDescriptor as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida">ConvertSidToStringSid</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertstringsidtosida">ConvertStringSidToSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd">MakeAbsoluteSD</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>
