---
UID: NF:winbase.ObjectOpenAuditAlarmA
title: ObjectOpenAuditAlarmA function
author: windows-sdk-content
description: Generates audit messages when a client application attempts to gain access to an object or to create a new one.
old-location: security\objectopenauditalarm.htm
old-project: SecAuthZ
ms.assetid: f3cb607b-a8fd-4a1b-9361-7ccd7cd8aac2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ObjectOpenAuditAlarm, ObjectOpenAuditAlarm function [Security], ObjectOpenAuditAlarmA, ObjectOpenAuditAlarmW, _win32_objectopenauditalarm, security.objectopenauditalarm, winbase/ObjectOpenAuditAlarm, winbase/ObjectOpenAuditAlarmA, winbase/ObjectOpenAuditAlarmW
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
req.unicode-ansi: ObjectOpenAuditAlarmW (Unicode) and ObjectOpenAuditAlarmA (ANSI)
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
-	ObjectOpenAuditAlarm
-	ObjectOpenAuditAlarmA
-	ObjectOpenAuditAlarmW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure for the object being accessed.


### -param ClientToken [in]

Identifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> representing the client requesting the operation. This handle must be obtained by opening the token of a thread impersonating the client. The token must be open for TOKEN_QUERY access.


### -param DesiredAccess [in]

Specifies the desired <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a>. This mask must have been previously mapped by the <a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a> function to contain no generic access rights.


### -param GrantedAccess [in]

Specifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> indicating which access rights are granted. This access mask is intended to be the same value set by one of the access-checking functions in its <i>GrantedAccess</i> parameter. Examples of access-checking functions include <a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a> and <a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>.


### -param Privileges [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551860">PRIVILEGE_SET</a> structure that specifies the set of <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> required for the access attempt. This parameter can be <b>NULL</b>.


### -param ObjectCreation [in]

Specifies a flag that determines whether the application creates a new object when access is granted. When this value is <b>TRUE</b>, the application creates a new object; when it is <b>FALSE</b>, the application opens an existing object.


### -param AccessGranted [in]

Specifies a flag indicating whether access was granted or denied in a previous call to an access-checking function, such as <a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>. If access was granted, this value is <b>TRUE</b>. If not, it is <b>FALSE</b>.


### -param GenerateOnClose [out]

A pointer to a flag set by the audit-generation routine when the function returns. This value must be passed to the 
<a href="https://msdn.microsoft.com/274f3a62-1833-402b-b362-f526b2bee14b">ObjectCloseAuditAlarm</a> function when the object handle is closed.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>ObjectOpenAuditAlarm</b> function requires the calling application to have the SE_AUDIT_NAME privilege enabled. The test for this privilege is always performed against the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> of the calling <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">process</a>, not the <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> of the thread. This allows the calling process to impersonate a client during the call.




## -see-also




<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a>



<a href="https://msdn.microsoft.com/91349693-8667-49dd-a813-657497b7d467">AreAllAccessesGranted</a>



<a href="https://msdn.microsoft.com/4bac6ebc-716a-4725-b9e6-a109b27dfc18">AreAnyAccessesGranted</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control</a>



<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a>



<a href="https://msdn.microsoft.com/274f3a62-1833-402b-b362-f526b2bee14b">ObjectCloseAuditAlarm</a>



<a href="https://msdn.microsoft.com/cb4c857c-5e63-41fe-8ae8-6762b0014a85">ObjectDeleteAuditAlarm</a>



<a href="https://msdn.microsoft.com/76714ffe-be7c-4928-b7c9-e72441ada4c7">ObjectPrivilegeAuditAlarm</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551860">PRIVILEGE_SET</a>



<a href="https://msdn.microsoft.com/a73d934a-1abf-4e60-bf0a-6c4629f28f7a">PrivilegeCheck</a>



<a href="https://msdn.microsoft.com/a424c583-bb71-4bda-a27f-2389b89104d8">PrivilegedServiceAuditAlarm</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>
 

 

