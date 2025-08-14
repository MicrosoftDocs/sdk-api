---
UID: NF:securitybaseapi.ObjectCloseAuditAlarmW
tech.root: security 
title: ObjectCloseAuditAlarmW
ms.date: 04/20/2021
targetos: Windows
description: Generates an audit message in the security event log when a handle to a private object is deleted. (ObjectCloseAuditAlarmW)
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
 - api-ms-win-downlevel-advapi32-l1-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - ObjectCloseAuditAlarmW
 - ObjectCloseAuditAlarm
f1_keywords:
 - ObjectCloseAuditAlarmW
 - securitybaseapi/ObjectCloseAuditAlarmW
 - ObjectCloseAuditAlarm
 - securitybaseapi/ObjectCloseAuditAlarm
dev_langs:
 - c++
---

# ObjectCloseAuditAlarmW function

## -description

The <b>ObjectCloseAuditAlarm</b> function generates an audit message in the security event log when a handle to a private object is deleted. Alarms are not currently supported.

## -parameters

### -param SubsystemName [in]

A pointer to a null-terminated string specifying the name of the subsystem calling the function. This string appears in any audit message that the function generates.

### -param HandleId [in]

A unique value representing the client's handle to the object. This should be the same value that was passed to the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckandauditalarmw">AccessCheckAndAuditAlarm</a> or <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-objectopenauditalarmw">ObjectOpenAuditAlarm</a> function.

### -param GenerateOnClose [in]

Specifies a flag set by a call to the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckandauditalarmw">AccessCheckAndAuditAlarm</a> or <b>ObjectCloseAuditAlarm</b> function when the object handle is created. If this flag is <b>TRUE</b>, the function generates an audit message. If it is <b>FALSE</b>, the function does not generate an audit message.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>ObjectCloseAuditAlarm</b> function requires the calling application to have the SE_AUDIT_NAME privilege enabled. The test for this privilege is always performed against the <a href="/windows/desktop/SecGloss/p-gly">primary token</a> of the calling <a href="/windows/desktop/SecGloss/p-gly">process</a>, allowing the calling process to impersonate a client

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>  
<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>  
<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>  
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-objectdeleteauditalarmw">ObjectDeleteAuditAlarm</a>  
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-objectopenauditalarmw">ObjectOpenAuditAlarm</a>  
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-objectprivilegeauditalarmw">ObjectPrivilegeAuditAlarm</a>  
