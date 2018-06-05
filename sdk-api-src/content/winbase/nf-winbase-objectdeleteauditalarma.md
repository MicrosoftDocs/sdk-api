---
UID: NF:winbase.ObjectDeleteAuditAlarmA
title: ObjectDeleteAuditAlarmA function
author: windows-sdk-content
description: Generates audit messages when an object is deleted.
old-location: security\objectdeleteauditalarm.htm
old-project: SecAuthZ
ms.assetid: cb4c857c-5e63-41fe-8ae8-6762b0014a85
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ObjectDeleteAuditAlarm, ObjectDeleteAuditAlarm function [Security], ObjectDeleteAuditAlarmA, ObjectDeleteAuditAlarmW, _win32_objectdeleteauditalarm, security.objectdeleteauditalarm, winbase/ObjectDeleteAuditAlarm, winbase/ObjectDeleteAuditAlarmA, winbase/ObjectDeleteAuditAlarmW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
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
-	ObjectDeleteAuditAlarm
-	ObjectDeleteAuditAlarmA
-	ObjectDeleteAuditAlarmW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ObjectDeleteAuditAlarmA function


## -description


The <b>ObjectDeleteAuditAlarm</b> function generates audit messages when an object is deleted. Alarms are not currently supported.


## -parameters




### -param SubsystemName [in]

A pointer to a null-terminated string specifying the name of the subsystem calling the function. This string appears in any audit message that the function generates.


### -param HandleId [in]

Specifies a unique value representing the client's handle to the object. This must be the same value that was passed to the 
<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a> or 
<a href="https://msdn.microsoft.com/f3cb607b-a8fd-4a1b-9361-7ccd7cd8aac2">ObjectOpenAuditAlarm</a> function.


### -param GenerateOnClose [in]

Specifies a flag set by a call to the 
<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a> or 
<a href="https://msdn.microsoft.com/f3cb607b-a8fd-4a1b-9361-7ccd7cd8aac2">ObjectOpenAuditAlarm</a> function when the object handle is created.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>ObjectDeleteAuditAlarm</b> function requires the calling application to have the SE_AUDIT_NAME privilege enabled. The test for this privilege is always performed against the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> of the calling <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">process</a>, allowing the calling process to impersonate a client.




## -see-also




<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a>



<a href="https://msdn.microsoft.com/91349693-8667-49dd-a813-657497b7d467">AreAllAccessesGranted</a>



<a href="https://msdn.microsoft.com/4bac6ebc-716a-4725-b9e6-a109b27dfc18">AreAnyAccessesGranted</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control</a>



<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a>



<a href="https://msdn.microsoft.com/274f3a62-1833-402b-b362-f526b2bee14b">ObjectCloseAuditAlarm</a>



<a href="https://msdn.microsoft.com/f3cb607b-a8fd-4a1b-9361-7ccd7cd8aac2">ObjectOpenAuditAlarm</a>



<a href="https://msdn.microsoft.com/76714ffe-be7c-4928-b7c9-e72441ada4c7">ObjectPrivilegeAuditAlarm</a>



<a href="https://msdn.microsoft.com/a73d934a-1abf-4e60-bf0a-6c4629f28f7a">PrivilegeCheck</a>



<a href="https://msdn.microsoft.com/a424c583-bb71-4bda-a27f-2389b89104d8">PrivilegedServiceAuditAlarm</a>
 

 

