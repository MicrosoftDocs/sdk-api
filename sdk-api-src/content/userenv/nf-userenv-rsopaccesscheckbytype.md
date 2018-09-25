---
UID: NF:userenv.RsopAccessCheckByType
title: RsopAccessCheckByType function
author: windows-sdk-content
description: The RSoPAccessCheckByType function determines whether a security descriptor grants a specified set of access rights to the client identified by an RSOPTOKEN.
old-location: policy\rsopaccesscheckbytype.htm
tech.root: Policy
ms.assetid: d63734a0-1a88-4669-828e-de467606fc14
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RSoPAccessCheckByType, RSoPAccessCheckByType function [Group Policy], RsopAccessCheckByType, _win32_rsopaccesscheckbytype, policy.rsopaccesscheckbytype, userenv/RSoPAccessCheckByType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - RSoPAccessCheckByType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RsopAccessCheckByType function


## -description


The
    <b>RSoPAccessCheckByType</b> function determines whether a security descriptor grants a specified set of access rights to the client identified by an <b>RSOPTOKEN</b>.


## -parameters




### -param pSecurityDescriptor [in]

Pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> against which access on the object is checked.


### -param pPrincipalSelfSid [in]

Pointer to a SID. If the security descriptor is associated with an object that represents a principal (for example, a user object), this parameter should be the SID of the object. When evaluating access, this SID logically replaces the SID in any ACE containing the well-known <b>PRINCIPAL_SELF</b> SID ("S-1-5-10"). For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa379571(v=VS.85).aspx">Security Identifiers</a> and 
<a href="https://msdn.microsoft.com/eb2f95c4-9465-409b-b76c-9ccae1d05eda">Well-Known SIDs</a>.

This parameter should be <b>NULL</b> if the protected object does not represent a principal.


### -param pRsopToken [in]

Pointer to a valid <b>RSOPTOKEN</b> representing the client attempting to gain access to the object.


### -param dwDesiredAccessMask [in]

Specifies an access mask that indicates the access rights to check. This mask can contain a combination of 
<a href="https://msdn.microsoft.com/e18cede9-9bf7-4866-850b-5d7fa43a5b0f">generic</a>, 
<a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">standard</a> and specific access rights. For more information, see 
<a href="https://msdn.microsoft.com/da67c486-d2e7-4632-ac7a-c18aabc3f21d">Access Rights and Access Masks</a>.


### -param pObjectTypeList [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/c729ff1a-65f3-4f6f-84dd-5700aead75ce">OBJECT_TYPE_LIST</a> structures that identify the hierarchy of object types for which to check access. Each element in the array specifies a <b>GUID</b> that identifies the object type and a value indicating the level of the object type in the hierarchy of object types. The array should not have two elements with the same <b>GUID</b>.

The array must have at least one element. The first element in the array must be at level zero and identify the object itself. The array can have only one level zero element. The second element is a subobject, such as a property set, at level 1. Following each level 1 entry are subordinate entries for the level 2 through 4 subobjects. Thus, the levels for the elements in the array might be {0, 1, 2, 2, 1, 2, 3}. If the object type list is out of order, 
<b>RSoPAccessCheckByType</b> fails and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INVALID_PARAMETER</b>.


### -param ObjectTypeListLength [in]

Specifies the number of elements in the <i>pObjectTypeList</i> array.


### -param pGenericMapping [in]

Pointer to the 
<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a> structure associated with the object for which access is being checked.


### -param pPrivilegeSet [in]

This parameter is currently unused.


### -param pdwPrivilegeSetLength [in]

This parameter is currently unused.


### -param pdwGrantedAccessMask [out]

Pointer to an 
<a href="https://msdn.microsoft.com/da67c486-d2e7-4632-ac7a-c18aabc3f21d">access mask</a> that receives the granted access rights.

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




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/dfdf14ee-fee1-4e96-9955-7f24dfe39487">RSoPFileAccessCheck</a>
 

 

