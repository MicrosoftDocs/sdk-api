---
UID: NF:winbase.AccessCheckAndAuditAlarmA
title: AccessCheckAndAuditAlarmA function (winbase.h)
description: Determines whether a security descriptor grants a specified set of access rights to the client being impersonated by the calling thread. (AccessCheckAndAuditAlarmA)
helpviewer_keywords: ["AccessCheckAndAuditAlarm","AccessCheckAndAuditAlarm function [Security]","AccessCheckAndAuditAlarmA","AccessCheckAndAuditAlarmW","_win32_accesscheckandauditalarm","security.accesscheckandauditalarm","winbase/AccessCheckAndAuditAlarm","winbase/AccessCheckAndAuditAlarmA","winbase/AccessCheckAndAuditAlarmW"]
old-location: security\accesscheckandauditalarm.htm
tech.root: security
ms.assetid: c2d144f4-9eeb-4723-9d28-97cfd1a07274
ms.date: 12/05/2018
ms.keywords: AccessCheckAndAuditAlarm, AccessCheckAndAuditAlarm function [Security], AccessCheckAndAuditAlarmA, AccessCheckAndAuditAlarmW, _win32_accesscheckandauditalarm, security.accesscheckandauditalarm, winbase/AccessCheckAndAuditAlarm, winbase/AccessCheckAndAuditAlarmA, winbase/AccessCheckAndAuditAlarmW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AccessCheckAndAuditAlarmW (Unicode) and AccessCheckAndAuditAlarmA (ANSI)
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
 - AccessCheckAndAuditAlarmA
 - winbase/AccessCheckAndAuditAlarmA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AccessCheckAndAuditAlarm
 - AccessCheckAndAuditAlarmA
 - AccessCheckAndAuditAlarmW
---

# AccessCheckAndAuditAlarmA function


## -description

The <b>AccessCheckAndAuditAlarm</b> function determines whether a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> grants a specified set of access rights to the client being impersonated by the calling thread. If the security descriptor has a SACL with ACEs that apply to the client, the function generates any necessary audit messages in the security event log.

Alarms are not currently supported.

## -parameters

### -param SubsystemName [in]

A pointer to a null-terminated string specifying the name of the subsystem calling the function. This string appears in any audit message that the function generates.

### -param HandleId [in, optional]

A pointer to a unique value representing the client's handle to the object. If the access is denied, the system ignores this value.

### -param ObjectTypeName [in]

A pointer to a null-terminated string specifying the type of object being created or accessed. This string appears in any audit message that the function generates.

### -param ObjectName [in, optional]

A pointer to a null-terminated string specifying the name of the object being created or accessed. This string appears in any audit message that the function generates.

### -param SecurityDescriptor [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure against which access is checked.

### -param DesiredAccess [in]

<a href="/windows/desktop/SecGloss/a-gly">Access mask</a> that specifies the access rights to check. This mask must have been mapped by the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a> function to contain no generic access rights. 




If this parameter is MAXIMUM_ALLOWED, the function sets the <i>GrantedAccess</i> access mask to indicate the maximum access rights the security descriptor allows the client.

### -param GenericMapping [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure associated with the object for which access is being checked.

### -param ObjectCreation [in]

Specifies a flag that determines whether the calling application will create a new object when access is granted. A value of <b>TRUE</b> indicates the application will create a new object. A value of <b>FALSE</b> indicates the application will open an existing object.

### -param GrantedAccess [out]

A pointer to an <a href="/windows/desktop/SecGloss/a-gly">access mask</a> that receives the granted access rights. If <i>AccessStatus</i> is set to <b>FALSE</b>, the function sets the access mask to zero. If the function fails, it does not set the access mask.

### -param AccessStatus [out]

A pointer to a variable that receives the results of the access check. If the security descriptor allows the requested access rights to the client, <i>AccessStatus</i> is set to <b>TRUE</b>. Otherwise, <i>AccessStatus</i> is set to <b>FALSE</b>.

### -param pfGenerateOnClose [out]

A pointer to a flag set by the audit-generation routine when the function returns. Pass this flag to the 
<a href="/windows/desktop/api/winbase/nf-winbase-objectcloseauditalarma">ObjectCloseAuditAlarm</a> function when the object handle is closed.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information, see the <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a> overview.

The <b>AccessCheckAndAuditAlarm</b> function requires the calling <a href="/windows/desktop/SecGloss/p-gly">process</a> to have the SE_AUDIT_NAME privilege enabled. The test for this privilege is performed against the <a href="/windows/desktop/SecGloss/p-gly">primary token</a> of the calling process, not the <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> of the thread.

The <b>AccessCheckAndAuditAlarm</b> function fails if the calling thread is not impersonating a client.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control </a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd">MakeAbsoluteSD</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectcloseauditalarma">ObjectCloseAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectopenauditalarma">ObjectOpenAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectprivilegeauditalarma">ObjectPrivilegeAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck">PrivilegeCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-privilegedserviceauditalarma">PrivilegedServiceAuditAlarm</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>
