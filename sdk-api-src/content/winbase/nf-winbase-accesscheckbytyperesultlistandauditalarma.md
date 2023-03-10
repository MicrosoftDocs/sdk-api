---
UID: NF:winbase.AccessCheckByTypeResultListAndAuditAlarmA
title: AccessCheckByTypeResultListAndAuditAlarmA function (winbase.h)
description: Determines whether a security descriptor grants a specified set of access rights to the client being impersonated by the calling thread. (AccessCheckByTypeResultListAndAuditAlarmA)
helpviewer_keywords: ["AccessCheckByTypeResultListAndAuditAlarm","AccessCheckByTypeResultListAndAuditAlarm function [Security]","AccessCheckByTypeResultListAndAuditAlarmA","AccessCheckByTypeResultListAndAuditAlarmW","_win32_accesscheckbytyperesultlistandauditalarm","security.accesscheckbytyperesultlistandauditalarm","winbase/AccessCheckByTypeResultListAndAuditAlarm","winbase/AccessCheckByTypeResultListAndAuditAlarmA","winbase/AccessCheckByTypeResultListAndAuditAlarmW"]
old-location: security\accesscheckbytyperesultlistandauditalarm.htm
tech.root: security
ms.assetid: 4b53a15a-5a6b-40c7-acf8-26b1f4bca4ae
ms.date: 12/05/2018
ms.keywords: AccessCheckByTypeResultListAndAuditAlarm, AccessCheckByTypeResultListAndAuditAlarm function [Security], AccessCheckByTypeResultListAndAuditAlarmA, AccessCheckByTypeResultListAndAuditAlarmW, _win32_accesscheckbytyperesultlistandauditalarm, security.accesscheckbytyperesultlistandauditalarm, winbase/AccessCheckByTypeResultListAndAuditAlarm, winbase/AccessCheckByTypeResultListAndAuditAlarmA, winbase/AccessCheckByTypeResultListAndAuditAlarmW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AccessCheckByTypeResultListAndAuditAlarmW (Unicode) and AccessCheckByTypeResultListAndAuditAlarmA (ANSI)
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
 - AccessCheckByTypeResultListAndAuditAlarmA
 - winbase/AccessCheckByTypeResultListAndAuditAlarmA
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
 - AccessCheckByTypeResultListAndAuditAlarm
 - AccessCheckByTypeResultListAndAuditAlarmA
 - AccessCheckByTypeResultListAndAuditAlarmW
---

# AccessCheckByTypeResultListAndAuditAlarmA function


## -description

The <b>AccessCheckByTypeResultListAndAuditAlarm</b> function determines whether a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> grants a specified set of access rights to the client being impersonated by the calling thread. The function can check access to a hierarchy of objects, such as an object, its property sets, and properties. The function reports the access rights granted or denied to each object type in the hierarchy. If the security descriptor has a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) with <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) that apply to the client, the function generates any necessary audit messages in the security event log. Alarms are not currently supported.

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
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure against which access is checked.

### -param PrincipalSelfSid [in, optional]

A pointer to a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID). If the security descriptor is associated with an object that represents a principal (for example, a user object), the <i>PrincipalSelfSid</i> parameter should be the SID of the object. When evaluating access, this SID logically replaces the SID in any ACE that contains the well-known PRINCIPAL_SELF SID (S-1-5-10). For information about well-known SIDs, see <a href="/windows/desktop/SecAuthZ/well-known-sids">Well-known SIDs</a>.

Set this parameter to <b>NULL</b> if the protected object does not represent a principal.

### -param DesiredAccess [in]

An <a href="/windows/desktop/SecGloss/a-gly">access mask</a> that specifies the access rights to check. This mask must have been mapped by the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a> function so that it contains no generic access rights.

If this parameter is MAXIMUM_ALLOWED, the function sets the access mask in <i>GrantedAccess</i> to indicate the maximum access rights the security descriptor allows the client.

### -param AuditType [in]

The type of audit to be generated. This can be one of the values from the 
<a href="/windows/desktop/api/winnt/ne-winnt-audit_event_type">AUDIT_EVENT_TYPE</a> enumeration type.

### -param Flags [in]

A flag that controls the function's behavior if the calling <a href="/windows/desktop/SecGloss/p-gly">process</a> does not have the SE_AUDIT_NAME privilege enabled. If the AUDIT_ALLOW_NO_PRIVILEGE flag is set, the function performs the access check without generating audit messages when the privilege is not enabled. If this parameter is zero, the function fails if the privilege is not enabled.

### -param ObjectTypeList [in, out, optional]

A pointer to an array of 
<a href="/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a> structures that identify the hierarchy of object types for which to check access. Each element in the array specifies a GUID that identifies the object type and a value that indicates the level of the object type in the hierarchy of object types. The array should not have two elements with the same GUID.

The array must have at least one element. The first element in the array must be at level zero and identify the object itself. The array can have only one level zero element. The second element is a subobject, such as a property set, at level 1. Following each level 1 entry are subordinate entries for the level 2 through 4 subobjects. Thus, the levels for the elements in the array might be {0, 1, 2, 2, 1, 2, 3}. If the object type list is out of order, <b>AccessCheckByTypeResultListAndAuditAlarm</b> fails, and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_PARAMETER.

### -param ObjectTypeListLength [in]

The number of elements in the <i>ObjectTypeList</i> array.

### -param GenericMapping [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure associated with the object for which access is being checked.

### -param ObjectCreation [in]

A flag that determines whether the calling application will create a new object when access is granted. A value of <b>TRUE</b> indicates the application will create a new object. A value of <b>FALSE</b> indicates the application will open an existing object.

### -param GrantedAccess [out]

A pointer to an array of access masks. The function sets each access mask to indicate the access rights granted to the corresponding element in the object type list. If the function fails, it does not set the access masks.

### -param AccessStatusList [out]

A pointer to an array of status codes for the corresponding elements in the object type list. The function sets an element to zero to indicate success or to a nonzero value to indicate the specific error during the access check. If the function fails, it does not set any of the elements in the array.

### -param pfGenerateOnClose [out]

A pointer to a flag set by the audit-generation routine when the function returns. Pass this flag to the 
<a href="/windows/desktop/api/winbase/nf-winbase-objectcloseauditalarma">ObjectCloseAuditAlarm</a> function when the object handle is closed.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information, see the <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a> overview.

The <b>AccessCheckByTypeResultListAndAuditAlarm</b> function is a combination of the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist">AccessCheckByTypeResultList</a> and 
<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a> functions.

The <i>ObjectTypeList</i> array does not necessarily represent the entire defined object. Rather, it represents that subset of the object for which to check access. For instance, to check access to two properties in a property set, specify an object type list with four elements: the object itself at level zero, the property set at level 1, and the two properties at level 2.

The <b>AccessCheckByTypeResultListAndAuditAlarm</b> function evaluates ACEs that apply to the object itself and object-specific ACEs for the object types listed in the <i>ObjectTypeList</i> array. The function ignores object-specific ACEs for object types not listed in the <i>ObjectTypeList</i> array.

For more information about how a hierarchy of ACEs controls access to an object and its subobjects, see 
<a href="/windows/desktop/SecAuthZ/aces-to-control-access-to-an-object-s-properties">ACEs to Control Access to an Object's Properties</a>.

To generate audit messages in the security event log, the calling process must have the SE_AUDIT_NAME privilege enabled. The system checks for this privilege in the <a href="/windows/desktop/SecGloss/p-gly">primary token</a> of the calling process, not the <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> of the thread. If the <i>Flags</i> parameter includes the AUDIT_ALLOW_NO_PRIVILEGE flag, the function performs the access check without generating audit messages when the privilege is not enabled.

The <b>AccessCheckByTypeResultListAndAuditAlarm</b> function fails if the calling thread is not impersonating a client.

If the security descriptor does not contain owner and group SIDs, <b>AccessCheckByTypeResultListAndAuditAlarm</b> fails with ERROR_INVALID_SECURITY_DESCR.

## -see-also

<a href="/windows/desktop/api/winnt/ne-winnt-audit_event_type">AUDIT_EVENT_TYPE</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype">AccessCheckByType</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist">AccessCheckByTypeResultList</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd">MakeAbsoluteSD</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>



<a href="/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectcloseauditalarma">ObjectCloseAuditAlarm</a>



<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>
