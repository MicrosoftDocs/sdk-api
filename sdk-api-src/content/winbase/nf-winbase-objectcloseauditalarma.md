---
UID: NF:winbase.ObjectCloseAuditAlarmA
title: ObjectCloseAuditAlarmA function
author: windows-driver-content
description: Generates an audit message in the security event log when a handle to a private object is deleted.
old-location: security\objectcloseauditalarm.htm
old-project: SecAuthZ
ms.assetid: 274f3a62-1833-402b-b362-f526b2bee14b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ObjectCloseAuditAlarm, ObjectCloseAuditAlarm function [Security], ObjectCloseAuditAlarmA, ObjectCloseAuditAlarmW, _win32_objectcloseauditalarm, security.objectcloseauditalarm, winbase/ObjectCloseAuditAlarm, winbase/ObjectCloseAuditAlarmA, winbase/ObjectCloseAuditAlarmW
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
req.unicode-ansi: ObjectCloseAuditAlarmW (Unicode) and ObjectCloseAuditAlarmA (ANSI)
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
-	ObjectCloseAuditAlarm
-	ObjectCloseAuditAlarmA
-	ObjectCloseAuditAlarmW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ObjectCloseAuditAlarmA function


## -description


The <b>ObjectCloseAuditAlarm</b> function generates an audit message in the security event log when a handle to a private object is deleted. Alarms are not currently supported.


## -parameters




### -param SubsystemName [in]

A pointer to a null-terminated string specifying the name of the subsystem calling the function. This string appears in any audit message that the function generates.


### -param HandleId [in]

A unique value representing the client's handle to the object. This should be the same value that was passed to the 
<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a> or <a href="https://msdn.microsoft.com/f3cb607b-a8fd-4a1b-9361-7ccd7cd8aac2">ObjectOpenAuditAlarm</a> function.


### -param GenerateOnClose [in]

Specifies a flag set by a call to the <a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a> or <b>ObjectCloseAuditAlarm</b> function when the object handle is created. If this flag is <b>TRUE</b>, the function generates an audit message. If it is <b>FALSE</b>, the function does not generate an audit message.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>ObjectCloseAuditAlarm</b> function requires the calling application to have the SE_AUDIT_NAME privilege enabled. The test for this privilege is always performed against the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> of the calling <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">process</a>, allowing the calling process to impersonate a client.




## -see-also




<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a>



<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/cb4c857c-5e63-41fe-8ae8-6762b0014a85">ObjectDeleteAuditAlarm</a>



<a href="https://msdn.microsoft.com/f3cb607b-a8fd-4a1b-9361-7ccd7cd8aac2">ObjectOpenAuditAlarm</a>



<a href="https://msdn.microsoft.com/76714ffe-be7c-4928-b7c9-e72441ada4c7">ObjectPrivilegeAuditAlarm</a>
 

 

