---
UID: NF:securitybaseapi.CreatePrivateObjectSecurity
title: CreatePrivateObjectSecurity function (securitybaseapi.h)
description: Allocates and initializes a self-relative security descriptor for a new private object. A protected server calls this function when it creates a new private object.
helpviewer_keywords: ["CreatePrivateObjectSecurity","CreatePrivateObjectSecurity function [Security]","_win32_createprivateobjectsecurity","security.createprivateobjectsecurity","securitybaseapi/CreatePrivateObjectSecurity"]
old-location: security\createprivateobjectsecurity.htm
tech.root: security
ms.assetid: 5f4832b6-5cf5-4050-9e20-56674f2e2cb1
ms.date: 12/05/2018
ms.keywords: CreatePrivateObjectSecurity, CreatePrivateObjectSecurity function [Security], _win32_createprivateobjectsecurity, security.createprivateobjectsecurity, securitybaseapi/CreatePrivateObjectSecurity
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
 - CreatePrivateObjectSecurity
 - securitybaseapi/CreatePrivateObjectSecurity
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
 - CreatePrivateObjectSecurity
---

# CreatePrivateObjectSecurity function


## -description

The <b>CreatePrivateObjectSecurity</b> function allocates and initializes a <a href="/windows/desktop/SecGloss/s-gly">self-relative security descriptor</a> for a new private object. A protected server calls this function when it creates a new private object.

To specify the object type GUID of the new object or control how <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) are inherited, use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurityex">CreatePrivateObjectSecurityEx</a> function.

## -parameters

### -param ParentDescriptor [in, optional]

A pointer to the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> for the parent directory in which a new object is being created. If there is no parent directory, this parameter can be <b>NULL</b>.

### -param CreatorDescriptor [in, optional]

A pointer to a security descriptor provided by the creator of the object. If the object's creator does not explicitly pass security information for the new object, this parameter is intended to be <b>NULL</b>.

### -param NewDescriptor [out]

A pointer to a variable that receives a pointer to the newly allocated self-relative security descriptor. The caller must call the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity">DestroyPrivateObjectSecurity</a> function to free this security descriptor.

### -param IsDirectoryObject [in]

Specifies whether the new object is a container. A value of <b>TRUE</b> indicates the object contains other objects, such as a directory.

### -param Token [in, optional]

A handle to the <a href="/windows/desktop/SecGloss/a-gly">access token</a> for the client <a href="/windows/desktop/SecGloss/p-gly">process</a> on whose behalf the object is being created. If this is an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>, it must be at SecurityIdentification level or higher. For a full description of the SecurityIdentification impersonation level, see the 
<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> enumerated type. 




A client token is used to retrieve default security information for the new object, such as its default owner, primary group, and <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a>. The token must be open for <b>TOKEN_QUERY</b> access.

If all of the following conditions are true, then the handle must be opened for <b>TOKEN_DUPLICATE</b> access in addition to <b>TOKEN_QUERY</b> access.

<ul>
<li>The token handle refers to a primary token.</li>
<li>The security descriptor of the token contains one or more ACEs with the <b>OwnerRights</b> SID.</li>
<li>A security descriptor is specified for the <i>CreatorDescriptor</i> parameter.</li>
<li>The caller of this function does not set the <b>SEF_AVOID_OWNER_RESTRICTION</b> flag in the <i>AutoInheritFlags</i> parameter.</li>
</ul>

### -param GenericMapping [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure that specifies the mapping from each generic right to specific rights for the object.

## -returns

If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) is specified in the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> specified by the <i>CreatorDescriptor</i> parameter, the <i>Token</i> parameter must have the SE_SECURITY_NAME privilege enabled. The <b>CreatePrivateObjectSecurity</b> function checks this privilege and may generate audits during the process.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurityex">CreatePrivateObjectSecurityEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity">DestroyPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity">GetPrivateObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a>