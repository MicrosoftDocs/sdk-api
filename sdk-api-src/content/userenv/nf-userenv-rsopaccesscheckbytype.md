---
UID: NF:userenv.RsopAccessCheckByType
title: RsopAccessCheckByType function (userenv.h)
description: The RSoPAccessCheckByType function determines whether a security descriptor grants a specified set of access rights to the client identified by an RSOPTOKEN.
helpviewer_keywords: ["RSoPAccessCheckByType","RSoPAccessCheckByType function [Group Policy]","RsopAccessCheckByType","_win32_rsopaccesscheckbytype","policy.rsopaccesscheckbytype","userenv/RSoPAccessCheckByType"]
old-location: policy\rsopaccesscheckbytype.htm
tech.root: Policy
ms.assetid: d63734a0-1a88-4669-828e-de467606fc14
ms.date: 12/05/2018
ms.keywords: RSoPAccessCheckByType, RSoPAccessCheckByType function [Group Policy], RsopAccessCheckByType, _win32_rsopaccesscheckbytype, policy.rsopaccesscheckbytype, userenv/RSoPAccessCheckByType
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RsopAccessCheckByType
 - userenv/RsopAccessCheckByType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - RSoPAccessCheckByType
---

# RsopAccessCheckByType function


## -description

The
    <b>RSoPAccessCheckByType</b> function determines whether a security descriptor grants a specified set of access rights to the client identified by an <b>RSOPTOKEN</b>.

## -parameters

### -param pSecurityDescriptor [in]

Pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> against which access on the object is checked.

### -param pPrincipalSelfSid [in]

Pointer to a SID. If the security descriptor is associated with an object that represents a principal (for example, a user object), this parameter should be the SID of the object. When evaluating access, this SID logically replaces the SID in any ACE containing the well-known <b>PRINCIPAL_SELF</b> SID ("S-1-5-10"). For more information, see 
<a href="/windows/desktop/SecAuthZ/security-identifiers">Security Identifiers</a> and 
<a href="/windows/desktop/SecAuthZ/well-known-sids">Well-Known SIDs</a>.

This parameter should be <b>NULL</b> if the protected object does not represent a principal.

### -param pRsopToken [in]

Pointer to a valid <b>RSOPTOKEN</b> representing the client attempting to gain access to the object.

### -param dwDesiredAccessMask [in]

Specifies an access mask that indicates the access rights to check. This mask can contain a combination of 
<a href="/windows/desktop/SecAuthZ/generic-access-rights">generic</a>, 
<a href="/windows/desktop/SecAuthZ/standard-access-rights">standard</a> and specific access rights. For more information, see 
<a href="/windows/desktop/SecAuthZ/access-rights-and-access-masks">Access Rights and Access Masks</a>.

### -param pObjectTypeList [in]

Pointer to an array of 
<a href="/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a> structures that identify the hierarchy of object types for which to check access. Each element in the array specifies a <b>GUID</b> that identifies the object type and a value indicating the level of the object type in the hierarchy of object types. The array should not have two elements with the same <b>GUID</b>.

The array must have at least one element. The first element in the array must be at level zero and identify the object itself. The array can have only one level zero element. The second element is a subobject, such as a property set, at level 1. Following each level 1 entry are subordinate entries for the level 2 through 4 subobjects. Thus, the levels for the elements in the array might be {0, 1, 2, 2, 1, 2, 3}. If the object type list is out of order, 
<b>RSoPAccessCheckByType</b> fails and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INVALID_PARAMETER</b>.

### -param ObjectTypeListLength [in]

Specifies the number of elements in the <i>pObjectTypeList</i> array.

### -param pGenericMapping [in]

Pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure associated with the object for which access is being checked.

### -param pPrivilegeSet [in]

This parameter is currently unused.

### -param pdwPrivilegeSetLength [in]

This parameter is currently unused.

### -param pdwGrantedAccessMask [out]

Pointer to an 
<a href="/windows/desktop/SecAuthZ/access-rights-and-access-masks">access mask</a> that receives the granted access rights.

If the function succeeds, the <i>pbAccessStatus</i> parameter is set to <b>TRUE</b>, and the mask is updated to contain the standard and specific rights granted. If <i>pbAccessStatus</i> is set to <b>FALSE</b>, this parameter is set to zero. If the function fails, the mask is not modified.

### -param pbAccessStatus [out]

Pointer to a variable that receives the results of the access check.

If the function succeeds, and the requested set of access rights are granted, this parameter is set to <b>TRUE</b>. Otherwise, this parameter is set to <b>FALSE</b>. If the function fails, the status is not modified.

## -returns

If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

The 
<b>RSoPAccessCheckByType</b> function compares the specified security descriptor with the specified <b>RSOPTOKEN</b> and indicates, in the <i>pbAccessStatus</i> parameter, whether access is granted or denied.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nf-userenv-rsopfileaccesscheck">RSoPFileAccessCheck</a>