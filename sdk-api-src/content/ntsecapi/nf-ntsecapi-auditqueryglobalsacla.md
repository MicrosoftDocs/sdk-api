---
UID: NF:ntsecapi.AuditQueryGlobalSaclA
title: AuditQueryGlobalSaclA function (ntsecapi.h)
description: Retrieves a global system access control list (SACL) that delegates access to the audit messages. (ANSI)
helpviewer_keywords: ["AuditQueryGlobalSaclA", "ntsecapi/AuditQueryGlobalSaclA"]
old-location: security\auditqueryglobalsacl.htm
tech.root: security
ms.assetid: 133BBC94-9C89-437A-9146-75A9898A6566
ms.date: 12/05/2018
ms.keywords: AuditQueryGlobalSacl, AuditQueryGlobalSacl function [Security], AuditQueryGlobalSaclA, AuditQueryGlobalSaclW, ntsecapi/AuditQueryGlobalSacl, ntsecapi/AuditQueryGlobalSaclA, ntsecapi/AuditQueryGlobalSaclW, security.auditqueryglobalsacl
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AuditQueryGlobalSaclW (Unicode) and AuditQueryGlobalSaclA (ANSI)
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
 - AuditQueryGlobalSaclA
 - ntsecapi/AuditQueryGlobalSaclA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-audit-l1-1-1.dll
 - sechost.dll
api_name:
 - AuditQueryGlobalSacl
 - AuditQueryGlobalSaclA
 - AuditQueryGlobalSaclW
---

# AuditQueryGlobalSaclA function


## -description

The <b>AuditQueryGlobalSacl</b> function retrieves  a global <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) that delegates access to the audit messages. Updating the global SACL requires the <b>SeSecurityPrivilege</b> which protects the global SACL from being updated by any user without administrator privileges.

## -parameters

### -param ObjectTypeName [in]

A pointer to a null-terminated string specifying the type of object being accessed. This parameter must be either "File" or "Key", depending on whether the object is a file or registry. This string appears in any audit message that the function generates.

### -param Acl [out]

A pointer to an <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure that contains the SACL information.  This should be freed later by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>GetLastError</b> may return one of the following error codes defined in WinError.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The caller does not have the privilege or access rights necessary to call this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87</dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -remarks

To successfully call this function, the caller must have <b>SeSecurityPrivilege</b>.




> [!NOTE]
> The ntsecapi.h header defines AuditQueryGlobalSacl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
