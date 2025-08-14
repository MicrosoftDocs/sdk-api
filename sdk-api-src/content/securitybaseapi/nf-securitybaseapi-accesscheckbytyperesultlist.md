---
UID: NF:securitybaseapi.AccessCheckByTypeResultList
title: AccessCheckByTypeResultList function (securitybaseapi.h)
description: Determines whether a security descriptor grants a specified set of access rights to the client identified by an access token. (AccessCheckByTypeResultList)
helpviewer_keywords: ["AccessCheckByTypeResultList","AccessCheckByTypeResultList function [Security]","_win32_accesscheckbytyperesultlist","security.accesscheckbytyperesultlist","securitybaseapi/AccessCheckByTypeResultList"]
old-location: security\accesscheckbytyperesultlist.htm
tech.root: security
ms.assetid: ce713421-d4ff-48ed-b751-5e5c5397d820
ms.date: 12/05/2018
ms.keywords: AccessCheckByTypeResultList, AccessCheckByTypeResultList function [Security], _win32_accesscheckbytyperesultlist, security.accesscheckbytyperesultlist, securitybaseapi/AccessCheckByTypeResultList
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
 - AccessCheckByTypeResultList
 - securitybaseapi/AccessCheckByTypeResultList
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
 - AccessCheckByTypeResultList
---

# AccessCheckByTypeResultList function


## -description

The <b>AccessCheckByTypeResultList</b> function determines whether a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> grants a specified set of access rights to the client identified by an <a href="/windows/desktop/SecGloss/a-gly">access token</a>. The function can check the client's access to a hierarchy of objects, such as an object, its property sets, and properties. The function reports the access rights granted or denied to each object type in the hierarchy. Typically, server applications use this function to check access to a private object.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure against which access is checked.

### -param PrincipalSelfSid [in, optional]

A pointer to a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID). If the security descriptor is associated with an object that represents a principal (for example, a user object), the <i>PrincipalSelfSid</i> parameter should be the SID of the object. When evaluating access, this SID logically replaces the SID in any <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) that contains the well-known PRINCIPAL_SELF SID (S-1-5-10). For information about well-known SIDs, see <a href="/windows/desktop/SecAuthZ/well-known-sids">Well-known SIDs</a>. 




If the protected object does not represent a principal, set this parameter to <b>NULL</b>.

### -param ClientToken [in]

A handle to an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> that represents the client attempting to gain access. The handle must have TOKEN_QUERY access to the token; otherwise, the function fails with ERROR_ACCESS_DENIED.

### -param DesiredAccess [in]

An <a href="/windows/desktop/SecGloss/a-gly">access mask</a> that specifies the access rights to check. This mask must have been mapped by the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a> function to contain no generic access rights. 




If this parameter is MAXIMUM_ALLOWED, the function sets the access masks in the <i>GrantedAccess</i> array to indicate the client's maximum access rights to each element in the object type list.

### -param ObjectTypeList [in, out, optional]

A pointer to an array of 
<a href="/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a> structures that identify the hierarchy of object types for which to check access. Each element in the array specifies a GUID that identifies the object type and a value that indicates the level of the object type in the hierarchy of object types. The array should not have two elements with the same GUID. 




The array must have at least one element. The first element in the array must be at level zero and identify the object itself. The array can have only one level zero element. The second element is a subobject, such as a property set, at level 1. Following each level 1 entry are subordinate entries for the level 2 through 4 subobjects. Thus, the levels for the elements in the array might be {0, 1, 2, 2, 1, 2, 3}. If the object type list is out of order, <b>AccessCheckByTypeResultList</b> fails and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_PARAMETER.

### -param ObjectTypeListLength [in]

The number of elements in the <i>ObjectTypeList</i> array. This is also the number of elements in the arrays pointed to by the <i>GrantedAccessList</i> and <i>AccessStatusList</i> parameters.

### -param GenericMapping [out]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure associated with the object for which access is being checked.

### -param PrivilegeSet [out, optional]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a> structure that receives the <a href="/windows/desktop/SecGloss/p-gly">privileges</a> used to perform the access validation. If no privileges were used, the function sets the <b>PrivilegeCount</b> member to zero.

### -param PrivilegeSetLength [in, out]

The size, in bytes, of the buffer pointed to by the <i>PrivilegeSet</i> parameter.

### -param GrantedAccessList [out]

A pointer to an array of access masks. The function sets each access mask to indicate the access rights granted to the corresponding element in the object type list. If the function fails, it does not set the access masks.

### -param AccessStatusList [out]

A pointer to an array of status codes for the corresponding elements in the object type list. The function sets an element to zero to indicate success or a nonzero value to indicate the specific error during the access check. If the function fails, it does not set any of the elements in the array.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information, see the <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a> overview.

The <b>AccessCheckByTypeResultList</b> function compares the specified security descriptor with the specified <a href="/windows/desktop/SecGloss/a-gly">access token</a> and indicates, in the <i>AccessStatusList</i> parameter, whether access is granted or denied for each of the elements in the object types list.

The <i>ObjectTypeList</i> array does not necessarily represent the entire defined object. Rather, it represents that subset of the object for which to check access. For instance, to check access to two properties in a property set, specify an object type list with four elements: the object itself at level zero, the property set at level 1, and the two properties at level 2.

The <b>AccessCheckByTypeResultList</b> function evaluates ACEs that apply to the object itself and object-specific ACEs for the object types listed in the <i>ObjectTypeList</i> array. The function ignores object-specific ACEs for object types not listed in the <i>ObjectTypeList</i> array. Thus, the results returned for element zero in the <i>AccessStatusList</i> parameter indicate the access allowed to the subset of the object defined by the <i>ObjectTypeList</i> parameter, not to the entire object.

For more information about how a hierarchy of ACEs controls access to an object and its subobjects, see 
<a href="/windows/desktop/SecAuthZ/aces-to-control-access-to-an-object-s-properties">ACEs to Control Access to an Object's Properties</a>.

If the security descriptor's <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) is <b>NULL</b>, the function grants the requested access to all of the elements in the object type list.

If the security descriptor does not contain owner and group SIDs, <b>AccessCheckByTypeResultList</b> fails with ERROR_INVALID_SECURITY_DESCR.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype">AccessCheckByType</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytypeandauditalarma">AccessCheckByTypeAndAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma">AccessCheckByTypeResultListAndAuditAlarm</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control </a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd">MakeAbsoluteSD</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>



<a href="/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a>



<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>
