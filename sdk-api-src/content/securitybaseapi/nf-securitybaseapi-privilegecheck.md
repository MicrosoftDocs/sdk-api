---
UID: NF:securitybaseapi.PrivilegeCheck
title: PrivilegeCheck function
author: windows-sdk-content
description: Determines whether a specified set of privileges are enabled in an access token.
old-location: security\privilegecheck.htm
tech.root: secauthz
ms.assetid: a73d934a-1abf-4e60-bf0a-6c4629f28f7a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PrivilegeCheck, PrivilegeCheck function [Security], _win32_privilegecheck, security.privilegecheck, securitybaseapi/PrivilegeCheck
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
 - PrivilegeCheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PrivilegeCheck function


## -description


The <b>PrivilegeCheck</b> function determines whether a specified set of 
<a href="https://msdn.microsoft.com/fe6aae0f-93eb-4aba-a6ac-45e71c251c51">privileges</a> are enabled in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>. The <b>PrivilegeCheck</b> function is typically called by a server application to check the privileges of a client's access token.


## -parameters




### -param ClientToken [in]

A handle to an access token representing a client <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a>. This handle must have been obtained by opening the token of a thread impersonating the client. The token must be open for TOKEN_QUERY access.


### -param RequiredPrivileges [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/2ee5615c-f684-4062-a6cb-e43e9de3a2fb">PRIVILEGE_SET</a> structure. The <b>Privilege</b> member of this structure is an array of 
<a href="https://msdn.microsoft.com/f337b561-4b67-42a0-b8de-06f546bafb26">LUID_AND_ATTRIBUTES</a> structures. Before calling <b>PrivilegeCheck</b>, use the <b>Privilege</b> array to indicate the set of privileges to check. Set the <b>Control</b> member to PRIVILEGE_SET_ALL_NECESSARY if all of the privileges must be enabled; or set it to zero if it is sufficient that any one of the privileges be enabled. 




When <b>PrivilegeCheck</b> returns, the <b>Attributes</b> member of each <a href="https://msdn.microsoft.com/f337b561-4b67-42a0-b8de-06f546bafb26">LUID_AND_ATTRIBUTES</a> structure is set to SE_PRIVILEGE_USED_FOR_ACCESS if the corresponding privilege is enabled.


### -param pfResult [out]

A pointer to a value the function sets to indicate whether any or all of the specified privileges are enabled in the access token. If the <b>Control</b> member of the <a href="https://msdn.microsoft.com/2ee5615c-f684-4062-a6cb-e43e9de3a2fb">PRIVILEGE_SET</a> structure specifies PRIVILEGE_SET_ALL_NECESSARY, this value is <b>TRUE</b> only if all the privileges are enabled; otherwise, this value is <b>TRUE</b> if any of the privileges are enabled.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



An access token contains a list of the privileges held by the account associated with the token. These privileges can be enabled or disabled; most are disabled by default. The <b>PrivilegeCheck</b> function checks only for enabled privileges. To get a list of all the enabled and disabled privileges held by an access token, call the 
<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function. To enable or disable a set of privileges in an access token, call the 
<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> function.




## -see-also




<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/f337b561-4b67-42a0-b8de-06f546bafb26">LUID_AND_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/334b8ba8-101d-43a1-a8bf-1c7e0448c272">LookupPrivilegeValue</a>



<a href="https://msdn.microsoft.com/76714ffe-be7c-4928-b7c9-e72441ada4c7">ObjectPrivilegeAuditAlarm</a>



<a href="https://msdn.microsoft.com/2ee5615c-f684-4062-a6cb-e43e9de3a2fb">PRIVILEGE_SET</a>



<a href="https://msdn.microsoft.com/a424c583-bb71-4bda-a27f-2389b89104d8">PrivilegedServiceAuditAlarm</a>
 

 

