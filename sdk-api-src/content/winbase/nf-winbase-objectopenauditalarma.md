---
UID: NF:winbase.ObjectOpenAuditAlarmA
title: ObjectOpenAuditAlarmA function (winbase.h)
description: Generates audit messages when a client application attempts to gain access to an object or to create a new one. (ObjectOpenAuditAlarmA)
helpviewer_keywords: ["ObjectOpenAuditAlarm","ObjectOpenAuditAlarm function [Security]","ObjectOpenAuditAlarmA","ObjectOpenAuditAlarmW","_win32_objectopenauditalarm","security.objectopenauditalarm","winbase/ObjectOpenAuditAlarm","winbase/ObjectOpenAuditAlarmA","winbase/ObjectOpenAuditAlarmW"]
old-location: security\objectopenauditalarm.htm
tech.root: security
ms.assetid: f3cb607b-a8fd-4a1b-9361-7ccd7cd8aac2
ms.date: 12/05/2018
ms.keywords: ObjectOpenAuditAlarm, ObjectOpenAuditAlarm function [Security], ObjectOpenAuditAlarmA, ObjectOpenAuditAlarmW, _win32_objectopenauditalarm, security.objectopenauditalarm, winbase/ObjectOpenAuditAlarm, winbase/ObjectOpenAuditAlarmA, winbase/ObjectOpenAuditAlarmW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ObjectOpenAuditAlarmW (Unicode) and ObjectOpenAuditAlarmA (ANSI)
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
 - ObjectOpenAuditAlarmA
 - winbase/ObjectOpenAuditAlarmA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - ObjectOpenAuditAlarm
 - ObjectOpenAuditAlarmA
 - ObjectOpenAuditAlarmW
---

# ObjectOpenAuditAlarmA function


## -description

The <b>ObjectOpenAuditAlarm</b> function generates audit messages when a client application attempts to gain access to an object or to create a new one. Alarms are not currently supported.

## -parameters

### -param SubsystemName [in]

A pointer to a <b>null</b>-terminated string specifying the name of the subsystem calling the function. This string appears in any audit message that the function generates.

### -param HandleId [in]

A pointer to a unique value representing the client's handle to the object. If the access is denied, this parameter is ignored.  




For cross-platform compatibility, the value addressed by this pointer must be sizeof(LPVOID) bytes long.

### -param ObjectTypeName [in]

A pointer to a <b>null</b>-terminated string specifying the type of object to which the client is requesting access. This string appears in any audit message that the function generates.

### -param ObjectName [in, optional]

A pointer to a <b>null</b>-terminated string specifying the name of the object to which the client is requesting access. This string appears in any audit message that the function generates.

### -param pSecurityDescriptor [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure for the object being accessed.

### -param ClientToken [in]

Identifies an <a href="/windows/desktop/SecGloss/a-gly">access token</a> representing the client requesting the operation. This handle must be obtained by opening the token of a thread impersonating the client. The token must be open for TOKEN_QUERY access.

### -param DesiredAccess [in]

Specifies the desired <a href="/windows/desktop/SecGloss/a-gly">access mask</a>. This mask must have been previously mapped by the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a> function to contain no generic access rights.

### -param GrantedAccess [in]

Specifies an <a href="/windows/desktop/SecGloss/a-gly">access mask</a> indicating which access rights are granted. This access mask is intended to be the same value set by one of the access-checking functions in its <i>GrantedAccess</i> parameter. Examples of access-checking functions include <a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>.

### -param Privileges [in, optional]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a> structure that specifies the set of <a href="/windows/desktop/SecGloss/p-gly">privileges</a> required for the access attempt. This parameter can be <b>NULL</b>.

### -param ObjectCreation [in]

Specifies a flag that determines whether the application creates a new object when access is granted. When this value is <b>TRUE</b>, the application creates a new object; when it is <b>FALSE</b>, the application opens an existing object.

### -param AccessGranted [in]

Specifies a flag indicating whether access was granted or denied in a previous call to an access-checking function, such as <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>. If access was granted, this value is <b>TRUE</b>. If not, it is <b>FALSE</b>.

### -param GenerateOnClose [out]

A pointer to a flag set by the audit-generation routine when the function returns. This value must be passed to the 
<a href="/windows/desktop/api/winbase/nf-winbase-objectcloseauditalarma">ObjectCloseAuditAlarm</a> function when the object handle is closed.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>ObjectOpenAuditAlarm</b> function requires the calling application to have the SE_AUDIT_NAME privilege enabled. The test for this privilege is always performed against the <a href="/windows/desktop/SecGloss/p-gly">primary token</a> of the calling <a href="/windows/desktop/SecGloss/p-gly">process</a>, not the <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> of the thread. This allows the calling process to impersonate a client during the call.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted">AreAllAccessesGranted</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted">AreAnyAccessesGranted</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectcloseauditalarma">ObjectCloseAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectdeleteauditalarma">ObjectDeleteAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectprivilegeauditalarma">ObjectPrivilegeAuditAlarm</a>



<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck">PrivilegeCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-privilegedserviceauditalarma">PrivilegedServiceAuditAlarm</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>
