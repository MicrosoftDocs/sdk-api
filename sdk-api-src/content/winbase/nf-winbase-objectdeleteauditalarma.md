---
UID: NF:winbase.ObjectDeleteAuditAlarmA
title: ObjectDeleteAuditAlarmA function (winbase.h)
description: The ObjectDeleteAuditAlarmA (ANSI) function (winbase.h) generates audit messages when an object is deleted.
helpviewer_keywords: ["ObjectDeleteAuditAlarm","ObjectDeleteAuditAlarm function [Security]","ObjectDeleteAuditAlarmA","ObjectDeleteAuditAlarmW","_win32_objectdeleteauditalarm","security.objectdeleteauditalarm","winbase/ObjectDeleteAuditAlarm","winbase/ObjectDeleteAuditAlarmA","winbase/ObjectDeleteAuditAlarmW"]
old-location: security\objectdeleteauditalarm.htm
tech.root: security
ms.assetid: cb4c857c-5e63-41fe-8ae8-6762b0014a85
ms.date: 08/04/2022
ms.keywords: ObjectDeleteAuditAlarm, ObjectDeleteAuditAlarm function [Security], ObjectDeleteAuditAlarmA, ObjectDeleteAuditAlarmW, _win32_objectdeleteauditalarm, security.objectdeleteauditalarm, winbase/ObjectDeleteAuditAlarm, winbase/ObjectDeleteAuditAlarmA, winbase/ObjectDeleteAuditAlarmW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ObjectDeleteAuditAlarmW (Unicode) and ObjectDeleteAuditAlarmA (ANSI)
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
 - ObjectDeleteAuditAlarmA
 - winbase/ObjectDeleteAuditAlarmA
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
 - ObjectDeleteAuditAlarm
 - ObjectDeleteAuditAlarmA
 - ObjectDeleteAuditAlarmW
---

# ObjectDeleteAuditAlarmA function


## -description

The <b>ObjectDeleteAuditAlarm</b> function generates audit messages when an object is deleted. Alarms are not currently supported.

## -parameters

### -param SubsystemName [in]

A pointer to a null-terminated string specifying the name of the subsystem calling the function. This string appears in any audit message that the function generates.

### -param HandleId [in]

Specifies a unique value representing the client's handle to the object. This must be the same value that was passed to the 
<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-objectopenauditalarma">ObjectOpenAuditAlarm</a> function.

### -param GenerateOnClose [in]

Specifies a flag set by a call to the 
<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-objectopenauditalarma">ObjectOpenAuditAlarm</a> function when the object handle is created.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>ObjectDeleteAuditAlarm</b> function requires the calling application to have the SE_AUDIT_NAME privilege enabled. The test for this privilege is always performed against the <a href="/windows/desktop/SecGloss/p-gly">primary token</a> of the calling <a href="/windows/desktop/SecGloss/p-gly">process</a>, allowing the calling process to impersonate a client.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted">AreAllAccessesGranted</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted">AreAnyAccessesGranted</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectcloseauditalarma">ObjectCloseAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectopenauditalarma">ObjectOpenAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectprivilegeauditalarma">ObjectPrivilegeAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck">PrivilegeCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-privilegedserviceauditalarma">PrivilegedServiceAuditAlarm</a>