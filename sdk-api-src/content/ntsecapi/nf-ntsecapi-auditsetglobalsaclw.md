---
UID: NF:ntsecapi.AuditSetGlobalSaclW
title: AuditSetGlobalSaclW function (ntsecapi.h)
description: Sets a global system access control list (SACL) that delegates access to the audit messages. (Unicode)
helpviewer_keywords: ["AuditSetGlobalSacl", "AuditSetGlobalSacl function [Security]", "AuditSetGlobalSaclW", "ntsecapi/AuditSetGlobalSacl", "ntsecapi/AuditSetGlobalSaclW", "security.auditsetglobalsacl"]
old-location: security\auditsetglobalsacl.htm
tech.root: security
ms.assetid: 48A41E3F-DDB0-431F-BCF0-E2452FEA57FA
ms.date: 12/05/2018
ms.keywords: AuditSetGlobalSacl, AuditSetGlobalSacl function [Security], AuditSetGlobalSaclA, AuditSetGlobalSaclW, ntsecapi/AuditSetGlobalSacl, ntsecapi/AuditSetGlobalSaclA, ntsecapi/AuditSetGlobalSaclW, security.auditsetglobalsacl
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AuditSetGlobalSaclW (Unicode) and AuditSetGlobalSaclA (ANSI)
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
 - AuditSetGlobalSaclW
 - ntsecapi/AuditSetGlobalSaclW
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
 - AuditSetGlobalSacl
 - AuditSetGlobalSaclA
 - AuditSetGlobalSaclW
---

# AuditSetGlobalSaclW function


## -description

The <b>AuditSetGlobalSacl</b> function sets a global <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) that delegates access to the audit messages. Updating the global SACL requires the <b>SeSecurityPrivilege</b> which protects the global SACL from being updated by any user without administrator privileges.

## -parameters

### -param ObjectTypeName [in]

A pointer to a null-terminated string specifying the type of object being created or accessed. For setting the global SACL on files, this should be set to "File" and  for setting the global SACL on registry, this should be set to "Key". This string appears in any audit message that the function generates.

### -param Acl [in, optional]

A pointer to an <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure.

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
> The ntsecapi.h header defines AuditSetGlobalSacl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
