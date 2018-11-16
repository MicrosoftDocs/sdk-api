---
UID: NF:winbase.AccessCheckAndAuditAlarmA
title: AccessCheckAndAuditAlarmA function
author: windows-sdk-content
description: Determines whether a security descriptor grants a specified set of access rights to the client being impersonated by the calling thread.
old-location: security\accesscheckandauditalarm.htm
tech.root: SecAuthZ
ms.assetid: c2d144f4-9eeb-4723-9d28-97cfd1a07274
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AccessCheckAndAuditAlarm, AccessCheckAndAuditAlarm function [Security], AccessCheckAndAuditAlarmA, AccessCheckAndAuditAlarmW, _win32_accesscheckandauditalarm, security.accesscheckandauditalarm, winbase/AccessCheckAndAuditAlarm, winbase/AccessCheckAndAuditAlarmA, winbase/AccessCheckAndAuditAlarmW
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
req.unicode-ansi: AccessCheckAndAuditAlarmW (Unicode) and AccessCheckAndAuditAlarmA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- AccessCheckAndAuditAlarmA
: 
---

# AccessCheckAndAuditAlarmA function


## -description


The <b>AccessCheckAndAuditAlarm</b> function determines whether a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> grants a specified set of access rights to the client being impersonated by the calling thread. If the security descriptor has a SACL with ACEs that apply to the client, the function generates any necessary audit messages in the security event log.

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
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure against which access is checked.


### -param DesiredAccess [in]

<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Access mask</a> that specifies the access rights to check. This mask must have been mapped by the 
<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a> function to contain no generic access rights. 




If this parameter is MAXIMUM_ALLOWED, the function sets the <i>GrantedAccess</i> access mask to indicate the maximum access rights the security descriptor allows the client.


### -param GenericMapping [in]

A pointer to the 
<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a> structure associated with the object for which access is being checked.


### -param ObjectCreation [in]

Specifies a flag that determines whether the calling application will create a new object when access is granted. A value of <b>TRUE</b> indicates the application will create a new object. A value of <b>FALSE</b> indicates the application will open an existing object.


### -param GrantedAccess [out]

A pointer to an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> that receives the granted access rights. If <i>AccessStatus</i> is set to <b>FALSE</b>, the function sets the access mask to zero. If the function fails, it does not set the access mask.


### -param AccessStatus [out]

A pointer to a variable that receives the results of the access check. If the security descriptor allows the requested access rights to the client, <i>AccessStatus</i> is set to <b>TRUE</b>. Otherwise, <i>AccessStatus</i> is set to <b>FALSE</b>.


### -param pfGenerateOnClose [out]

A pointer to a flag set by the audit-generation routine when the function returns. Pass this flag to the 
<a href="https://msdn.microsoft.com/274f3a62-1833-402b-b362-f526b2bee14b">ObjectCloseAuditAlarm</a> function when the object handle is closed.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For more information, see the <a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a> overview.

The <b>AccessCheckAndAuditAlarm</b> function requires the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> to have the SE_AUDIT_NAME privilege enabled. The test for this privilege is performed against the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> of the calling process, not the <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> of the thread.

The <b>AccessCheckAndAuditAlarm</b> function fails if the calling thread is not impersonating a client.




## -see-also




<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control </a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a>



<a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a>



<a href="https://msdn.microsoft.com/47c75071-f10d-43cf-a841-2dd49fc39afa">MakeAbsoluteSD</a>



<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a>



<a href="https://msdn.microsoft.com/274f3a62-1833-402b-b362-f526b2bee14b">ObjectCloseAuditAlarm</a>



<a href="https://msdn.microsoft.com/f3cb607b-a8fd-4a1b-9361-7ccd7cd8aac2">ObjectOpenAuditAlarm</a>



<a href="https://msdn.microsoft.com/76714ffe-be7c-4928-b7c9-e72441ada4c7">ObjectPrivilegeAuditAlarm</a>



<a href="https://msdn.microsoft.com/a73d934a-1abf-4e60-bf0a-6c4629f28f7a">PrivilegeCheck</a>



<a href="https://msdn.microsoft.com/a424c583-bb71-4bda-a27f-2389b89104d8">PrivilegedServiceAuditAlarm</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>
 

 

