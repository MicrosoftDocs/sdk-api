---
UID: NF:securitybaseapi.ConvertToAutoInheritPrivateObjectSecurity
title: ConvertToAutoInheritPrivateObjectSecurity function (securitybaseapi.h)
description: Converts a security descriptor and its access control lists (ACLs) to a format that supports automatic propagation of inheritable access control entries (ACEs).
helpviewer_keywords: ["ConvertToAutoInheritPrivateObjectSecurity","ConvertToAutoInheritPrivateObjectSecurity function [Security]","_win32_converttoautoinheritprivateobjectsecurity","security.converttoautoinheritprivateobjectsecurity","securitybaseapi/ConvertToAutoInheritPrivateObjectSecurity"]
old-location: security\converttoautoinheritprivateobjectsecurity.htm
tech.root: security
ms.assetid: eaaa5509-eff5-461d-843b-7ebbbe0dd58f
ms.date: 12/05/2018
ms.keywords: ConvertToAutoInheritPrivateObjectSecurity, ConvertToAutoInheritPrivateObjectSecurity function [Security], _win32_converttoautoinheritprivateobjectsecurity, security.converttoautoinheritprivateobjectsecurity, securitybaseapi/ConvertToAutoInheritPrivateObjectSecurity
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
 - ConvertToAutoInheritPrivateObjectSecurity
 - securitybaseapi/ConvertToAutoInheritPrivateObjectSecurity
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
 - ConvertToAutoInheritPrivateObjectSecurity
---

# ConvertToAutoInheritPrivateObjectSecurity function


## -description

The <b>ConvertToAutoInheritPrivateObjectSecurity</b> function converts a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> and its <a href="/windows/desktop/SecGloss/a-gly">access control lists</a> (ACLs) to a format that supports automatic propagation of inheritable <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs).

## -parameters

### -param ParentDescriptor [in, optional]

A pointer to the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> for the parent container of the object. If there is no parent container, this parameter is <b>NULL</b>.

### -param CurrentSecurityDescriptor [in]

A pointer to the current security descriptor of the object.

### -param NewSecurityDescriptor [out]

A pointer to a variable that receives a pointer to the newly allocated <a href="/windows/desktop/SecGloss/s-gly">self-relative security descriptor</a>. It is the caller's responsibility to call the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity">DestroyPrivateObjectSecurity</a> function to free this security descriptor.

### -param ObjectType [in, optional]

A pointer to a 
<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the type of object associated with the <i>CurrentSecurityDescriptor</i> parameter. If the object does not have a GUID, this parameter must be <b>NULL</b>.

### -param IsDirectoryObject [in]

If <b>TRUE</b>, the new object is a container and can contain other objects. If <b>FALSE</b>, the new object is not a container.

### -param GenericMapping [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure that specifies the mapping from each generic right to specific rights for the object.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>ConvertToAutoInheritPrivateObjectSecurity</b> function attempts to determine whether the ACEs in the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) and <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) of the current security descriptor were inherited from the parent security descriptor. The function passes the <i>ParentDescriptor</i> parameter to the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurityex">CreatePrivateObjectSecurityEx</a> function to get ACLs that contain only inherited ACEs. Then it compares these ACEs to the ACEs in the original security descriptor to determine which of the original ACEs were inherited. The ACEs do not need to match one-to-one. For instance, an ACE that allows read and write access to a trustee can be equivalent to two ACEs: an ACE that allows read access and an ACE that allows write access.

Any ACEs in the original security descriptor that are equivalent to the ACEs inherited from the parent security descriptor are marked with the INHERITED_ACE flag and added to the new security descriptor. All other ACEs in the original security descriptor are added to the new security descriptor as noninherited ACEs.

If the original DACL does not have any inherited ACEs, the function sets the SE_DACL_PROTECTED flag in the control bits of the new security descriptor. Similarly, the SE_SACL_PROTECTED flag is set if none of the ACEs in the SACL is inherited.

For DACLs that have inherited ACEs, the function reorders the ACEs into two groups. The first group has ACEs that were directly applied to the object. The second group has inherited ACEs. This ordering ensures that noninherited ACEs have precedence over inherited ACEs. For more information, see 
<a href="/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl">Order of ACEs in a DACL</a>.

The function sets the SE_DACL_AUTO_INHERITED and SE_SACL_AUTO_INHERITED flags in the control bits of the new security descriptor.

The function does not change the ordering of access-allowed ACEs in relation to access-denied ACEs in the DACL because to do so would change the semantics of the resulting security descriptor. If the function cannot convert the DACL without changing the semantics, it leaves the DACL unchanged and sets the SE_DACL_PROTECTED flag.

The new security descriptor has the same owner and primary group as the original security descriptor.

The new security descriptor is equivalent to the original security descriptor, so the caller needs no access rights or <a href="/windows/desktop/SecGloss/p-gly">privileges</a> to update the security descriptor to the new format.

This function works with ACL_REVISION and ACL_REVISION_DS ACLs.

## -see-also

<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurityex">CreatePrivateObjectSecurityEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity">DestroyPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>