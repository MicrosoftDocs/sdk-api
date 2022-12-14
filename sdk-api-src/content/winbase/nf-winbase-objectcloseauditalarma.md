---
UID: NF:winbase.ObjectCloseAuditAlarmA
title: ObjectCloseAuditAlarmA function (winbase.h)
description: Generates an audit message in the security event log when a handle to a private object is deleted. (ObjectCloseAuditAlarmA)
helpviewer_keywords: ["ObjectCloseAuditAlarm","ObjectCloseAuditAlarm function [Security]","ObjectCloseAuditAlarmA","ObjectCloseAuditAlarmW","_win32_objectcloseauditalarm","security.objectcloseauditalarm","winbase/ObjectCloseAuditAlarm","winbase/ObjectCloseAuditAlarmA","winbase/ObjectCloseAuditAlarmW"]
old-location: security\objectcloseauditalarm.htm
tech.root: security
ms.assetid: 274f3a62-1833-402b-b362-f526b2bee14b
ms.date: 12/05/2018
ms.keywords: ObjectCloseAuditAlarm, ObjectCloseAuditAlarm function [Security], ObjectCloseAuditAlarmA, ObjectCloseAuditAlarmW, _win32_objectcloseauditalarm, security.objectcloseauditalarm, winbase/ObjectCloseAuditAlarm, winbase/ObjectCloseAuditAlarmA, winbase/ObjectCloseAuditAlarmW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ObjectCloseAuditAlarmW (Unicode) and ObjectCloseAuditAlarmA (ANSI)
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
 - ObjectCloseAuditAlarmA
 - winbase/ObjectCloseAuditAlarmA
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
 - ObjectCloseAuditAlarm
 - ObjectCloseAuditAlarmA
 - ObjectCloseAuditAlarmW
---

# ObjectCloseAuditAlarmA function


## -description

The <b>ObjectCloseAuditAlarm</b> function generates an audit message in the security event log when a handle to a private object is deleted. Alarms are not currently supported.

## -parameters

### -param SubsystemName [in]

A pointer to a null-terminated string specifying the name of the subsystem calling the function. This string appears in any audit message that the function generates.

### -param HandleId [in]

A unique value representing the client's handle to the object. This should be the same value that was passed to the 
<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a> or <a href="/windows/desktop/api/winbase/nf-winbase-objectopenauditalarma">ObjectOpenAuditAlarm</a> function.

### -param GenerateOnClose [in]

Specifies a flag set by a call to the <a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a> or <b>ObjectCloseAuditAlarm</b> function when the object handle is created. If this flag is <b>TRUE</b>, the function generates an audit message. If it is <b>FALSE</b>, the function does not generate an audit message.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>ObjectCloseAuditAlarm</b> function requires the calling application to have the SE_AUDIT_NAME privilege enabled. The test for this privilege is always performed against the <a href="/windows/desktop/SecGloss/p-gly">primary token</a> of the calling <a href="/windows/desktop/SecGloss/p-gly">process</a>, allowing the calling process to impersonate a client.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectdeleteauditalarma">ObjectDeleteAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectopenauditalarma">ObjectOpenAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectprivilegeauditalarma">ObjectPrivilegeAuditAlarm</a>
