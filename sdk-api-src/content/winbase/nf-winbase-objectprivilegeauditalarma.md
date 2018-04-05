---
UID: NF:winbase.ObjectPrivilegeAuditAlarmA
title: ObjectPrivilegeAuditAlarmA function
author: windows-driver-content
description: Generates an audit message in the security event log.
old-location: security\objectprivilegeauditalarm.htm
old-project: SecAuthZ
ms.assetid: 76714ffe-be7c-4928-b7c9-e72441ada4c7
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: ObjectPrivilegeAuditAlarm, ObjectPrivilegeAuditAlarm function [Security], ObjectPrivilegeAuditAlarmA, ObjectPrivilegeAuditAlarmW, _win32_objectprivilegeauditalarm, security.objectprivilegeauditalarm, winbase/ObjectPrivilegeAuditAlarm, winbase/ObjectPrivilegeAuditAlarmA, winbase/ObjectPrivilegeAuditAlarmW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ObjectPrivilegeAuditAlarmW (Unicode) and ObjectPrivilegeAuditAlarmA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
-	KernelBase.dll
-	API-MS-Win-Security-base-l1-1-0.dll
-	API-MS-Win-Security-base-l1-2-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Security-Base-L1-2-1.dll
api_name:
-	ObjectPrivilegeAuditAlarm
-	ObjectPrivilegeAuditAlarmA
-	ObjectPrivilegeAuditAlarmW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ObjectPrivilegeAuditAlarmA function


## -description


The <b>ObjectPrivilegeAuditAlarm</b> function generates an audit message in the security event log. A protected server can use this function to log attempts by a client to use a specified set of <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> with an open handle to a private object. Alarms are not currently supported.


## -parameters




### -param SubsystemName [in]

A pointer to a null-terminated string specifying the name of the subsystem calling the function. This string appears in the audit message.


### -param HandleId [in]

A pointer to a unique value representing the client's handle to the object.


### -param ClientToken [in]

Identifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> representing the client that requested the operation. This handle must have been obtained by opening the token of a thread impersonating the client. The token must be open for TOKEN_QUERY access. The function uses this token to get the identity of the client for the audit message.


### -param DesiredAccess [in]

Specifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> indicating the privileged access types being used or whose use is being attempted. The access mask can be mapped by the 
<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a> function so it does not contain any generic access types.


### -param Privileges [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551860">PRIVILEGE_SET</a> structure containing the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> that the client attempted to use. The names of the privileges appear in the audit message.


### -param AccessGranted [in]

Indicates whether the client's attempt to use the privileges was successful. If this value is <b>TRUE</b>, the audit message indicates success. If this value is <b>FALSE</b>, the audit message indicates failure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>ObjectPrivilegeAuditAlarm</b> function does not check the client's access to the object or check the client's access token to determine whether the privileges are held or enabled. Typically, you call the 
<a href="https://msdn.microsoft.com/a73d934a-1abf-4e60-bf0a-6c4629f28f7a">PrivilegeCheck</a> function to determine whether the specified privileges are enabled in the access token, call the 
<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a> function to check the client's access to the object, and then call <b>ObjectPrivilegeAuditAlarm</b> to log the results.

The <b>ObjectPrivilegeAuditAlarm</b> function requires the calling <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">process</a> to have SE_AUDIT_NAME privilege enabled. The test for this privilege is always performed against the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> of the calling process, not the <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> of the thread. This allows the calling process to impersonate a client during the call.




## -see-also




<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a>



<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a>



<a href="https://msdn.microsoft.com/274f3a62-1833-402b-b362-f526b2bee14b">ObjectCloseAuditAlarm</a>



<a href="https://msdn.microsoft.com/f3cb607b-a8fd-4a1b-9361-7ccd7cd8aac2">ObjectOpenAuditAlarm</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551860">PRIVILEGE_SET</a>



<a href="https://msdn.microsoft.com/a73d934a-1abf-4e60-bf0a-6c4629f28f7a">PrivilegeCheck</a>



<a href="https://msdn.microsoft.com/a424c583-bb71-4bda-a27f-2389b89104d8">PrivilegedServiceAuditAlarm</a>
 

 

