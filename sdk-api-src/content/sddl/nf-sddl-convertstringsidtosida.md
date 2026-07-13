---
UID: NF:sddl.ConvertStringSidToSidA
title: ConvertStringSidToSidA function (sddl.h)
description: Converts a string-format security identifier (SID) into a valid, functional SID. You can use this function to retrieve a SID that the ConvertSidToStringSid function converted to string format. (ANSI)
helpviewer_keywords: ["ConvertStringSidToSidA", "sddl/ConvertStringSidToSidA"]
old-location: security\convertstringsidtosid.htm
tech.root: security
ms.assetid: bf7262e3-ad2c-44c4-99cb-dcf29ad36efd
ms.date: 12/05/2018
ms.keywords: ConvertStringSidToSid, ConvertStringSidToSid function [Security], ConvertStringSidToSidA, ConvertStringSidToSidW, _win32_convertstringsidtosid, sddl/ConvertStringSidToSid, sddl/ConvertStringSidToSidA, sddl/ConvertStringSidToSidW, security.convertstringsidtosid
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ConvertStringSidToSidA
 - sddl/ConvertStringSidToSidA
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
 - ConvertStringSidToSid
 - ConvertStringSidToSidA
 - ConvertStringSidToSidW
---

# ConvertStringSidToSidA function


## -description

The <b>ConvertStringSidToSid</b> function converts a string-format <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) into a valid, functional SID. You can use this function to retrieve a SID that the 
<a href="/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida">ConvertSidToStringSid</a> function converted to string format.

## -parameters

### -param StringSid [in]

A pointer to a null-terminated string containing the string-format SID to convert. 


The SID string can use either the standard 
							S-<i>R</i>-<i>I</i>-<i>S</i>-<i>S</i>… format for SID strings, or the SID string constant format, such as "BA" for  built-in administrators. For more information about SID string notation, see 
<a href="/windows/desktop/SecAuthZ/sid-components">SID Components</a>.

### -param Sid [out]

A pointer to a variable that receives a pointer to the converted SID. To free the returned buffer, call the 
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

<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida">ConvertSidToStringSid</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora">ConvertStringSecurityDescriptorToSecurityDescriptor</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>

## -remarks

> [!NOTE]
> The sddl.h header defines ConvertStringSidToSid as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
