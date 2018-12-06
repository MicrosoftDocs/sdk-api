---
UID: NF:securitybaseapi.AccessCheck
title: AccessCheck function
author: windows-sdk-content
description: Determines whether a security descriptor grants a specified set of access rights to the client identified by an access token.
old-location: security\accesscheck.htm
tech.root: secauthz
ms.assetid: d9fd2e44-5782-40c9-a1cf-1788ca7afc50
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AccessCheck, AccessCheck function [Security], _win32_accesscheck, security.accesscheck, securitybaseapi/AccessCheck
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - AccessCheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AccessCheck function


## -description


The <b>AccessCheck</b> function determines whether a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> grants a specified set of access rights to the client identified by an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>. Typically, server applications use this function to check access to a private object.


## -parameters




### -param pSecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure against which access is checked.


### -param ClientToken [in]

A handle to an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> that represents the client that is attempting to gain access. The handle must have TOKEN_QUERY access to the token; otherwise, the function fails with ERROR_ACCESS_DENIED.


### -param DesiredAccess [in]

<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Access mask</a> that specifies the access rights to check. This mask must have been mapped by the 
<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a> function to contain no generic access rights. 




If this parameter is MAXIMUM_ALLOWED, the function sets the <i>GrantedAccess</i> access mask to indicate the maximum access rights the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> allows the client.


### -param GenericMapping [in]

A pointer to the 
<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a> structure associated with the object for which access is being checked.


### -param PrivilegeSet [out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/2ee5615c-f684-4062-a6cb-e43e9de3a2fb">PRIVILEGE_SET</a> structure that receives the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privileges</a> used to perform the access validation. If no privileges were used, the function sets the <b>PrivilegeCount</b> member to zero.


### -param PrivilegeSetLength [in, out]

Specifies the size, in bytes, of the buffer pointed to by the <i>PrivilegeSet</i> parameter.


### -param GrantedAccess [out]

A pointer to an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> that receives the granted access rights. If <i>AccessStatus</i> is set to <b>FALSE</b>, the function sets the access mask to zero. If the function fails, it does not set the access mask.


### -param AccessStatus [out]

A pointer to a variable that receives the results of the access check. If the security descriptor allows the requested access rights to the client identified by the access token, <i>AccessStatus</i> is set to <b>TRUE</b>. Otherwise, <i>AccessStatus</i> is set to <b>FALSE</b>, and you can call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to get extended error information.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For more information, see the <a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a> overview.

The <b>AccessCheck</b> function compares the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> with the specified access token and indicates, in the <i>AccessStatus</i> parameter, whether access is granted or denied. If access is granted, the requested <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> becomes the object's granted access mask.

If the security descriptor's DACL is <b>NULL</b>, the <i>AccessStatus</i> parameter returns <b>TRUE</b>, which indicates that the client has the requested access.

The <b>AccessCheck</b> function fails with ERROR_INVALID_SECURITY_DESCR if the security descriptor does not contain owner and group SIDs.

The <b>AccessCheck</b> function does not generate an audit. If your application  requires audits for access checks, use functions such as  <a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a>, <a href="https://msdn.microsoft.com/ea14fd55-e0e4-4bf2-b20e-5874783c16c3">AccessCheckByTypeAndAuditAlarm</a>, <a href="https://msdn.microsoft.com/4b53a15a-5a6b-40c7-acf8-26b1f4bca4ae">AccessCheckByTypeResultListAndAuditAlarm</a>, or <a href="https://msdn.microsoft.com/7d3ddce4-40a2-483d-8cff-48d89313b383">AccessCheckByTypeResultListAndAuditAlarmByHandle</a>, instead of  <b>AccessCheck</b>.


#### Examples

For an example that uses this function, see 
     <a href="https://msdn.microsoft.com/de21968e-4590-4798-9152-43204d55521f">Verifying Client Access with ACLs</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a>



<a href="https://msdn.microsoft.com/91349693-8667-49dd-a813-657497b7d467">AreAllAccessesGranted</a>



<a href="https://msdn.microsoft.com/4bac6ebc-716a-4725-b9e6-a109b27dfc18">AreAnyAccessesGranted</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control </a>



<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a>



<a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a>



<a href="https://msdn.microsoft.com/47c75071-f10d-43cf-a841-2dd49fc39afa">MakeAbsoluteSD</a>



<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a>



<a href="https://msdn.microsoft.com/2ee5615c-f684-4062-a6cb-e43e9de3a2fb">PRIVILEGE_SET</a>



<a href="https://msdn.microsoft.com/a73d934a-1abf-4e60-bf0a-6c4629f28f7a">PrivilegeCheck</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>
 

 

