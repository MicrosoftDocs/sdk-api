---
UID: NF:securitybaseapi.PrivilegedServiceAuditAlarmW
tech.root: security 
title: PrivilegedServiceAuditAlarmW
ms.date: 04/20/2021
targetos: Windows
description: Generates an audit message in the security event log.  (PrivilegedServiceAuditAlarmW)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Advapi32.dll 
req.header: securitybaseapi.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: Advapi32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - PrivilegedServiceAuditAlarmW
 - PrivilegedServiceAuditAlarm
f1_keywords:
 - PrivilegedServiceAuditAlarmW
 - securitybaseapi/PrivilegedServiceAuditAlarmW
 - PrivilegedServiceAuditAlarm
 - securitybaseapi/PrivilegedServiceAuditAlarm
dev_langs:
 - c++
---

# PrivilegedServiceAuditAlarmW function

## -description

The <b>PrivilegedServiceAuditAlarm</b> function generates an audit message in the security event log. A protected server can use this function to log attempts by a client to use a specified set of <a href="/windows/desktop/SecGloss/p-gly">privileges</a>.

Alarms are not currently supported.

## -parameters

### -param SubsystemName [in]

A pointer to a null-terminated string specifying the name of the subsystem calling the function. This information appears in the security event log record.

### -param ServiceName [in]

A pointer to a null-terminated string specifying the name of the privileged subsystem service. This information appears in the security event log record.

### -param ClientToken [in]

Identifies an <a href="/windows/desktop/SecGloss/a-gly">access token</a> representing the client that requested the operation. This handle must have been obtained by opening the token of a thread impersonating the client. The token must be open for TOKEN_QUERY access. The function uses this token to get the identity of the client for the security event log record.

### -param Privileges [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a> structure containing the privileges that the client attempted to use. The names of the privileges appear in the security event log record.

### -param AccessGranted [in]

Indicates whether the client's attempt to use the privileges was successful. If this value is <b>TRUE</b>, the security event log record indicates success. If this value is <b>FALSE</b>, the security event log record indicates failure.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>PrivilegedServiceAuditAlarm</b> function does not check the client's access token to determine whether the privileges are held or enabled. Typically, you first call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck">PrivilegeCheck</a> function to determine whether the specified privileges are enabled in the access token, and then call <b>PrivilegedServiceAuditAlarm</b> to log the results.

The <b>PrivilegedServiceAuditAlarm</b> function requires the calling process to have SE_AUDIT_NAME privilege enabled. The test for this privilege is always performed against the <a href="/windows/desktop/SecGloss/p-gly">primary token</a> of the calling process. This allows the calling process to impersonate a client during the call.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>  
<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>  
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-objectprivilegeauditalarmw">ObjectPrivilegeAuditAlarm</a>  
<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a>  
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck">PrivilegeCheck</a>  
