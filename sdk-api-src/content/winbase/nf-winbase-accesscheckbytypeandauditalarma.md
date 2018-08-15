---
UID: NF:winbase.AccessCheckByTypeAndAuditAlarmA
title: AccessCheckByTypeAndAuditAlarmA function
author: windows-sdk-content
description: Determines whether a security descriptor grants a specified set of access rights to the client being impersonated by the calling thread.
old-location: security\accesscheckbytypeandauditalarm.htm
old-project: secauthz
ms.assetid: ea14fd55-e0e4-4bf2-b20e-5874783c16c3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AccessCheckByTypeAndAuditAlarm, AccessCheckByTypeAndAuditAlarm function [Security], AccessCheckByTypeAndAuditAlarmA, AccessCheckByTypeAndAuditAlarmW, _win32_accesscheckbytypeandauditalarm, security.accesscheckbytypeandauditalarm, winbase/AccessCheckByTypeAndAuditAlarm, winbase/AccessCheckByTypeAndAuditAlarmA, winbase/AccessCheckByTypeAndAuditAlarmW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AccessCheckByTypeAndAuditAlarmW (Unicode) and AccessCheckByTypeAndAuditAlarmA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
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
 - AccessCheckByTypeAndAuditAlarm
 - AccessCheckByTypeAndAuditAlarmA
 - AccessCheckByTypeAndAuditAlarmW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# AccessCheckByTypeAndAuditAlarmA function


## -description


The <b>AccessCheckByTypeAndAuditAlarm</b> function determines whether a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> grants a specified set of access rights to the client being impersonated by the calling thread. The function can check the client's access to a hierarchy of objects, such as an object, its property sets, and properties. The function grants or denies access to the hierarchy as a whole. If the security descriptor has a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) with <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) that apply to the client, the function generates any necessary audit messages in the security event log.

Alarms are not currently supported.


## -parameters




### -param SubsystemName [in]

A pointer to a null-terminated string that specifies the name of the subsystem calling the function. This string appears in any audit message that the function generates.


### -param HandleId [in]

A pointer to a unique value that represents the client's handle to the object. If the access is denied, the system ignores this value.


### -param ObjectTypeName [in]

A pointer to a null-terminated string that specifies the type of object being created or accessed. This string appears in any audit message that the function generates.


### -param ObjectName [in, optional]

A pointer to a null-terminated string that specifies the name of the object being created or accessed. This string appears in any audit message that the function generates.


### -param SecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure against which access is checked.


### -param PrincipalSelfSid [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID). If the security descriptor is associated with an object that represents a principal (for example, a user object), the <i>PrincipalSelfSid</i> parameter should be the SID of the object. When evaluating access, this SID logically replaces the SID in any ACE containing the well-known PRINCIPAL_SELF SID (S-1-5-10). For information about well-known SIDs, see <a href="https://msdn.microsoft.com/eb2f95c4-9465-409b-b76c-9ccae1d05eda">Well-known SIDs</a>. 




If the protected object does not represent a principal, set this parameter to <b>NULL</b>.


### -param DesiredAccess [in]

An <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> that specifies the access rights to check. This mask must have been mapped by the 
<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a> function to contain no generic access rights. 




If this parameter is MAXIMUM_ALLOWED, the function sets the <i>GrantedAccess</i> access mask to indicate the maximum access rights the security descriptor allows the client.


### -param AuditType [in]

The type of audit to be generated. This can be one of the values from the 
<a href="https://msdn.microsoft.com/7dc21840-6dcc-445b-a254-f8ca27008d63">AUDIT_EVENT_TYPE</a> enumeration type.


### -param Flags [in]

A flag that controls the function's behavior if the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> does not have the SE_AUDIT_NAME privilege enabled. If the AUDIT_ALLOW_NO_PRIVILEGE flag is set, the function performs the access check without generating audit messages when the privilege is not enabled. If this parameter is zero, the function fails if the privilege is not enabled.


### -param ObjectTypeList [in, out, optional]

A pointer to an array of 
<a href="https://msdn.microsoft.com/c729ff1a-65f3-4f6f-84dd-5700aead75ce">OBJECT_TYPE_LIST</a> structures that identify the hierarchy of object types for which to check access. Each element in the array specifies a GUID that identifies the object type and a value that indicates the level of the object type in the hierarchy of object types. The array should not have two elements with the same GUID. 




The array must have at least one element. The first element in the array must be at level zero and identify the object itself. The array can have only one level zero element. The second element is a subobject, such as a property set, at level 1. Following each level 1 entry are subordinate entries for the level 2 through 4 subobjects. Thus, the levels for the elements in the array might be {0, 1, 2, 2, 1, 2, 3}. If the object type list is out of order, <b>AccessCheckByTypeAndAuditAlarm</b> fails and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INVALID_PARAMETER.


### -param ObjectTypeListLength [in]

The number of elements in the <i>ObjectTypeList</i> array.


### -param GenericMapping [in]

A pointer to the 
<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a> structure associated with the object for which access is being checked.


### -param ObjectCreation [in]

A flag that determines whether the calling application will create a new object when access is granted. A value of <b>TRUE</b> indicates the application will create a new object. A value of <b>FALSE</b> indicates the application will open an existing object.


### -param GrantedAccess [out]

A pointer to an access mask that receives the granted access rights. If <i>AccessStatus</i> is set to <b>FALSE</b>, the function sets the access mask to zero. If the function fails, it does not set the access mask.


### -param AccessStatus [out]

A pointer to a variable that receives the results of the access check. If the security descriptor allows the requested access rights to the client, <i>AccessStatus</i> is set to <b>TRUE</b>. Otherwise, <i>AccessStatus</i> is set to <b>FALSE</b> and you can call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to get extended error information.


### -param pfGenerateOnClose [out]

A pointer to a flag set by the audit-generation routine when the function returns. Pass this flag to the 
<a href="https://msdn.microsoft.com/274f3a62-1833-402b-b362-f526b2bee14b">ObjectCloseAuditAlarm</a> function when the object handle is closed.


## -returns



If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For more information, see the <a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a> overview.

If the <i>PrincipalSelfSid</i> and <i>ObjectTypeList</i> parameters are <b>NULL</b>, the <i>AuditType</i> parameter is <i>AuditEventObjectAccess</i>, and the <i>Flags</i> parameter is zero, <b>AccessCheckByTypeAndAuditAlarm</b> performs in the same way as the 
<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a> function.

The <i>ObjectTypeList</i> array does not necessarily represent the entire defined object. Rather, it represents that subset of the object for which to check access. For instance, to check access to two properties in a property set, specify an object type list with four elements: the object itself at level zero, the property set at level 1, and the two properties at level 2.

The <b>AccessCheckByTypeAndAuditAlarm</b> function evaluates ACEs that apply to the object itself and object-specific ACEs for the object types listed in the <i>ObjectTypeList</i> array. The function ignores object-specific ACEs for object types not listed in the <i>ObjectTypeList</i> array. Thus, the results returned in the <i>AccessStatus</i> parameter indicate the access allowed to the subset of the object defined by the <i>ObjectTypeList</i> parameter, not to the entire object.

For more information about how a hierarchy of ACEs controls access to an object and its subobjects, see 
<a href="https://msdn.microsoft.com/79dd4a45-c42c-4775-93ce-6e3206894d63">ACEs to Control Access to an Object's Properties</a>.

To generate audit messages in the security event log, the calling process must have the SE_AUDIT_NAME privilege enabled. The system checks for this privilege in the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> of the calling process, not the <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> of the thread. If the <i>Flags</i> parameter includes the AUDIT_ALLOW_NO_PRIVILEGE flag, the function performs the access check without generating audit messages when the privilege is not enabled.

The <b>AccessCheckByTypeAndAuditAlarm</b> function fails if the calling thread is not impersonating a client.

If the security descriptor does not contain owner and group SIDs, <b>AccessCheckByTypeAndAuditAlarm</b> fails with ERROR_INVALID_SECURITY_DESCR.




## -see-also




<a href="https://msdn.microsoft.com/7dc21840-6dcc-445b-a254-f8ca27008d63">AUDIT_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a>



<a href="https://msdn.microsoft.com/50acfc17-459d-464c-9927-88b32dd424c7">AccessCheckByType</a>



<a href="https://msdn.microsoft.com/ce713421-d4ff-48ed-b751-5e5c5397d820">AccessCheckByTypeResultList</a>



<a href="https://msdn.microsoft.com/4b53a15a-5a6b-40c7-acf8-26b1f4bca4ae">AccessCheckByTypeResultListAndAuditAlarm</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control </a>



<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a>



<a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a>



<a href="https://msdn.microsoft.com/47c75071-f10d-43cf-a841-2dd49fc39afa">MakeAbsoluteSD</a>



<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a>



<a href="https://msdn.microsoft.com/c729ff1a-65f3-4f6f-84dd-5700aead75ce">OBJECT_TYPE_LIST</a>



<a href="https://msdn.microsoft.com/274f3a62-1833-402b-b362-f526b2bee14b">ObjectCloseAuditAlarm</a>



<a href="https://msdn.microsoft.com/2ee5615c-f684-4062-a6cb-e43e9de3a2fb">PRIVILEGE_SET</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>
 

 

