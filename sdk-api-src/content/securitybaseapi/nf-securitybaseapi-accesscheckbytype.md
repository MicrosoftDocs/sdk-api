---
UID: NF:securitybaseapi.AccessCheckByType
title: AccessCheckByType function (securitybaseapi.h)
description: Determines whether a security descriptor grants a specified set of access rights to the client identified by an access token. (AccessCheckByType)
helpviewer_keywords: ["AccessCheckByType","AccessCheckByType function [Security]","_win32_accesscheckbytype","security.accesscheckbytype","securitybaseapi/AccessCheckByType"]
old-location: security\accesscheckbytype.htm
tech.root: security
ms.assetid: 50acfc17-459d-464c-9927-88b32dd424c7
ms.date: 12/05/2018
ms.keywords: AccessCheckByType, AccessCheckByType function [Security], _win32_accesscheckbytype, security.accesscheckbytype, securitybaseapi/AccessCheckByType
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - AccessCheckByType
 - securitybaseapi/AccessCheckByType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AccessCheckByType
---

# AccessCheckByType function


## -description

The <b>AccessCheckByType</b> function determines whether a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> grants a specified set of access rights to the client identified by an <a href="/windows/desktop/SecGloss/a-gly">access token</a>. The function can check the client's access to a hierarchy of objects, such as an object, its property sets, and properties. The function grants or denies access to the hierarchy as a whole. Typically, server applications use this function to check access to a private object.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure against which access is checked.

### -param PrincipalSelfSid [in, optional]

A pointer to a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID). If the security descriptor is associated with an object that represents a principal (for example, a user object), the <i>PrincipalSelfSid</i> parameter should be the SID of the object. When evaluating access, this SID logically replaces the SID in any <a href="/windows/desktop/SecGloss/a-gly">access control entry</a>  containing the well-known PRINCIPAL_SELF SID (S-1-5-10). For information about well-known SIDs, see <a href="/windows/desktop/SecAuthZ/well-known-sids">Well-known SIDs</a>. 




Set this parameter to <b>NULL</b> if the protected object does not represent a principal.

### -param ClientToken [in]

A handle to an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> that represents the client attempting to gain access. The handle must have TOKEN_QUERY access to the token; otherwise, the function fails with ERROR_ACCESS_DENIED.

### -param DesiredAccess [in]

<a href="/windows/desktop/SecGloss/a-gly">Access mask</a> that specifies the access rights to check. This mask must have been mapped by the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a> function to contain no generic access rights. 




If this parameter is MAXIMUM_ALLOWED, the function sets the <i>GrantedAccess</i> access mask to indicate the maximum access rights the security descriptor allows the client.

### -param ObjectTypeList [in, out, optional]

A pointer to an array of 
<a href="/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a> structures that identify the hierarchy of object types for which to check access. Each element in the array specifies a GUID that identifies the object type and a value indicating the level of the object type in the hierarchy of object types. The array should not have two elements with the same GUID. 




The array must have at least one element. The first element in the array must be at level zero and identify the object itself. The array can have only one level zero element. The second element is a subobject, such as a property set, at level 1. Following each level 1 entry are subordinate entries for the level 2 through 4 subobjects. Thus, the levels for the elements in the array might be {0, 1, 2, 2, 1, 2, 3}. If the object type list is out of order, <b>AccessCheckByType</b> fails and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_PARAMETER.

If <i>ObjectTypeList</i> is <b>NULL</b>, <b>AccessCheckByType</b> is the same as the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a> function.

### -param ObjectTypeListLength [in]

Specifies the number of elements in the <i>ObjectTypeList</i> array.

### -param GenericMapping [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure associated with the object for which access is being checked. The <b>GenericAll</b> member of the  <b>GENERIC_MAPPING</b> structure should contain all the access rights that can be granted by the resource manager, including STANDARD_RIGHTS_ALL and all of the rights that are set in the <b>GenericRead</b>, <b>GenericWrite</b>, and <b>GenericExecute</b> members.

### -param PrivilegeSet [out, optional]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a> structure that receives the <a href="/windows/desktop/SecGloss/p-gly">privileges</a> used to perform the access validation. If no privileges were used, the function sets the <b>PrivilegeCount</b> member to zero.

### -param PrivilegeSetLength [in, out]

Specifies the size, in bytes, of the buffer pointed to by the <i>PrivilegeSet</i> parameter.

### -param GrantedAccess [out]

A pointer to an access mask that receives the granted access rights. If <i>AccessStatus</i> is set to <b>FALSE</b>, the function sets the access mask to zero. If the function fails, it does not set the access mask.

### -param AccessStatus [out]

A pointer to a variable that receives the results of the access check. If the security descriptor allows the requested access rights to the client identified by the access token, <i>AccessStatus</i> is set to <b>TRUE</b>. Otherwise, <i>AccessStatus</i> is set to <b>FALSE</b>, and you can call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information, see the <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a> overview.

The <b>AccessCheckByType</b> function compares the specified security descriptor with the specified access token and indicates, in the <i>AccessStatus</i> parameter, whether access is granted or denied.

The <i>ObjectTypeList</i> array does not necessarily represent the entire defined object. Rather, it represents that subset of the object for which to check access. For instance, to check access to two properties in a property set, specify an object type list with four elements: the object itself at level zero, the property set at level 1, and the two properties at level 2.

The <b>AccessCheckByType</b> function evaluates ACEs that apply to the object itself and object-specific ACEs for the object types listed in the <i>ObjectTypeList</i> array. The function ignores object-specific ACEs for object types not listed in the <i>ObjectTypeList</i> array. Thus, the results returned in the <i>AccessStatus</i> parameter indicate the access allowed to the subset of the object defined by the <i>ObjectTypeList</i> parameter, not to the entire object.

For more information about how a hierarchy of ACEs controls access to an object and its subobjects, see 
<a href="/windows/desktop/SecAuthZ/aces-to-control-access-to-an-object-s-properties">ACEs to Control Access to an Object's Properties</a>.

If the security descriptor's DACL is <b>NULL</b>, the <i>AccessStatus</i> parameter returns <b>TRUE</b>, indicating that the client has the requested access.

If the security descriptor does not contain owner and group SIDs, <b>AccessCheckByType</b> fails with ERROR_INVALID_SECURITY_DESCR.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytypeandauditalarma">AccessCheckByTypeAndAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist">AccessCheckByTypeResultList</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma">AccessCheckByTypeResultListAndAuditAlarm</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd">MakeAbsoluteSD</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>



<a href="/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a>



<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>
