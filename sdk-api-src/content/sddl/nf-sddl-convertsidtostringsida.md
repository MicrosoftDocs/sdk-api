---
UID: NF:sddl.ConvertSidToStringSidA
title: ConvertSidToStringSidA function (sddl.h)
description: Converts a security identifier (SID) to a string format suitable for display, storage, or transmission. (ANSI)
helpviewer_keywords: ["ConvertSidToStringSidA", "sddl/ConvertSidToStringSidA"]
old-location: security\convertsidtostringsid.htm
tech.root: security
ms.assetid: e673e727-edb1-450c-9e1a-a3dc90acc929
ms.date: 12/05/2018
ms.keywords: ConvertSidToStringSid, ConvertSidToStringSid function [Security], ConvertSidToStringSidA, ConvertSidToStringSidW, _win32_convertsidtostringsid, sddl/ConvertSidToStringSid, sddl/ConvertSidToStringSidA, sddl/ConvertSidToStringSidW, security.convertsidtostringsid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ConvertSidToStringSidA
 - sddl/ConvertSidToStringSidA
dev_langs:
 - c++
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
---

# ConvertSidToStringSidA function


## -description

The <b>ConvertSidToStringSid</b> function converts a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) to a string format suitable for display, storage, or transmission.

To convert the string-format SID back to a valid, functional SID, call the 
<a href="/windows/desktop/api/sddl/nf-sddl-convertstringsidtosida">ConvertStringSidToSid</a> function.

## -parameters

### -param Sid [in]

A pointer to the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure to be converted.

### -param StringSid [out]

A pointer to a variable that receives a pointer to a null-terminated SID string. To free the returned buffer, call the 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The <b>GetLastError</b> function may return one of the following error codes.

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
<a href="/windows/desktop/SecAuthZ/sid-components">SID Components</a>.





> [!NOTE]
> The sddl.h header defines ConvertSidToStringSid as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora">ConvertStringSecurityDescriptorToSecurityDescriptor</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertstringsidtosida">ConvertStringSidToSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>
