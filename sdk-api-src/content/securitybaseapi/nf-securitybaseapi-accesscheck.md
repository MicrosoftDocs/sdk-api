---
UID: NF:securitybaseapi.AccessCheck
title: AccessCheck function (securitybaseapi.h)
description: Determines whether a security descriptor grants a specified set of access rights to the client identified by an access token. (AccessCheck)
helpviewer_keywords: ["AccessCheck","AccessCheck function [Security]","_win32_accesscheck","security.accesscheck","securitybaseapi/AccessCheck"]
old-location: security\accesscheck.htm
tech.root: security
ms.assetid: d9fd2e44-5782-40c9-a1cf-1788ca7afc50
ms.date: 12/05/2018
ms.keywords: AccessCheck, AccessCheck function [Security], _win32_accesscheck, security.accesscheck, securitybaseapi/AccessCheck
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
 - AccessCheck
 - securitybaseapi/AccessCheck
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
 - AccessCheck
---

# AccessCheck function


## -description

The <b>AccessCheck</b> function determines whether a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> grants a specified set of access rights to the client identified by an <a href="/windows/desktop/SecGloss/a-gly">access token</a>. Typically, server applications use this function to check access to a private object.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure against which access is checked.

### -param ClientToken [in]

A handle to an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> that represents the client that is attempting to gain access. The handle must have TOKEN_QUERY access to the token; otherwise, the function fails with ERROR_ACCESS_DENIED.

### -param DesiredAccess [in]

<a href="/windows/desktop/SecGloss/a-gly">Access mask</a> that specifies the access rights to check. This mask must have been mapped by the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a> function to contain no generic access rights. 




If this parameter is MAXIMUM_ALLOWED, the function sets the <i>GrantedAccess</i> access mask to indicate the maximum access rights the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> allows the client.

### -param GenericMapping [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure associated with the object for which access is being checked.

### -param PrivilegeSet [out, optional]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a> structure that receives the <a href="/windows/desktop/SecGloss/p-gly">privileges</a> used to perform the access validation. If no privileges were used, the function sets the <b>PrivilegeCount</b> member to zero.

### -param PrivilegeSetLength [in, out]

Specifies the size, in bytes, of the buffer pointed to by the <i>PrivilegeSet</i> parameter.

### -param GrantedAccess [out]

A pointer to an <a href="/windows/desktop/SecGloss/a-gly">access mask</a> that receives the granted access rights. If <i>AccessStatus</i> is set to <b>FALSE</b>, the function sets the access mask to zero. If the function fails, it does not set the access mask.

### -param AccessStatus [out]

A pointer to a variable that receives the results of the access check. If the security descriptor allows the requested access rights to the client identified by the access token, <i>AccessStatus</i> is set to <b>TRUE</b>. Otherwise, <i>AccessStatus</i> is set to <b>FALSE</b>, and you can call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information.

## -returns

If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information, see the <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a> overview.

The <b>AccessCheck</b> function compares the specified <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> with the specified access token and indicates, in the <i>AccessStatus</i> parameter, whether access is granted or denied. If access is granted, the requested <a href="/windows/desktop/SecGloss/a-gly">access mask</a> becomes the object's granted access mask.

If the security descriptor's DACL is <b>NULL</b>, the <i>AccessStatus</i> parameter returns <b>TRUE</b>, which indicates that the client has the requested access.

The <b>AccessCheck</b> function fails with ERROR_INVALID_SECURITY_DESCR if the security descriptor does not contain owner and group SIDs.

The <b>AccessCheck</b> function does not generate an audit. If your application  requires audits for access checks, use functions such as  <a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>, <a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytypeandauditalarma">AccessCheckByTypeAndAuditAlarm</a>, <a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma">AccessCheckByTypeResultListAndAuditAlarm</a>, or <a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea">AccessCheckByTypeResultListAndAuditAlarmByHandle</a>, instead of  <b>AccessCheck</b>.


#### Examples

For an example that uses this function, see 
     <a href="/windows/desktop/SecAuthZ/verifying-client-access-with-acls-in-c--">Verifying Client Access with ACLs</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted">AreAllAccessesGranted</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted">AreAnyAccessesGranted</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control </a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd">MakeAbsoluteSD</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>



<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck">PrivilegeCheck</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>
