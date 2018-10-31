---
UID: NF:securitybaseapi.GetTokenInformation
title: GetTokenInformation function
author: windows-sdk-content
description: Retrieves a specified type of information about an access token. The calling process must have appropriate access rights to obtain the information.
old-location: security\gettokeninformation.htm
tech.root: secauthz
ms.assetid: e94de19c-de12-40fb-a72c-060f7ad12f75
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetTokenInformation, GetTokenInformation function [Security], _win32_gettokeninformation, security.gettokeninformation, securitybaseapi/GetTokenInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetTokenInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTokenInformation function


## -description


The <b>GetTokenInformation</b> function retrieves a specified type of information about an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>. The calling process must have appropriate access rights to obtain the information.

To determine if a user is a member of a specific group, use the 
<a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a> function. To determine group membership for app container tokens, use the <a href="https://msdn.microsoft.com/0420FC77-8035-42A5-8907-83D0CE53FB64">CheckTokenMembershipEx</a> function.


## -parameters




### -param TokenHandle [in]

A handle to an access token from which information is retrieved. If <i>TokenInformationClass</i> specifies TokenSource, the handle must have TOKEN_QUERY_SOURCE access. For all other <i>TokenInformationClass</i> values, the handle must have TOKEN_QUERY access.


### -param TokenInformationClass [in]

Specifies a value from the 
<a href="https://msdn.microsoft.com/cb606665-1266-4e71-a145-9b04bf157cdc">TOKEN_INFORMATION_CLASS</a> enumerated type to identify the type of information the function retrieves. Any callers who check the <b>TokenIsAppContainer</b> and have it return 0 should also verify that the caller token is not an identify level impersonation token. If the current token is not an app container but is an identity level token, you should return <b>AccessDenied</b>.


### -param TokenInformation [out, optional]

A pointer to a buffer the function fills with the requested information. The structure put into this buffer depends upon the type of information specified by the <i>TokenInformationClass</i> parameter.


### -param TokenInformationLength [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>TokenInformation</i> parameter. If <i>TokenInformation</i> is <b>NULL</b>, this parameter must be zero.


### -param ReturnLength [out]

A pointer to a variable that receives the number of bytes needed for the buffer pointed to by the <i>TokenInformation</i> parameter. If this value is larger than the value specified in the <i>TokenInformationLength</i> parameter, the function fails and stores no data in the buffer.

If the value of the <i>TokenInformationClass</i> parameter is TokenDefaultDacl and the token has no default DACL, the function sets the variable pointed to by <i>ReturnLength</i> to <code>sizeof(</code><a href="https://msdn.microsoft.com/29fb738f-1ecd-4b72-9aea-64698cd74c12">TOKEN_DEFAULT_DACL</a><code>)</code> and sets the <b>DefaultDacl</b> member of the <b>TOKEN_DEFAULT_DACL</b> structure to <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/839c4b58-4c61-4f72-8337-1e3dfa267ee5">AdjustTokenGroups</a>



<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a>



<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>



<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a>



<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a>



<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a>



<a href="https://msdn.microsoft.com/29fb738f-1ecd-4b72-9aea-64698cd74c12">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/085ccd0a-d6c2-48ca-ad2a-933f22831b14">TOKEN_GROUPS_AND_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/cb606665-1266-4e71-a145-9b04bf157cdc">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/85617d56-ad46-40a3-a335-121f3c8edcc3">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/d23ebe6c-36a3-434a-a0fa-fcdf50dd19a0">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/c9016511-740f-44f3-92ed-17cc518c6612">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/9c533327-e4a0-4852-828c-622d190b7d1e">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/7fcc4a46-1bac-49c1-a239-b466d3bf31d9">TOKEN_STATISTICS</a>



<a href="https://msdn.microsoft.com/51b6717e-3fda-4af4-8995-4ac571eae2fd">TOKEN_TYPE</a>



<a href="https://msdn.microsoft.com/5dd8172d-7b1a-4cc0-b667-5fe91d278393">TOKEN_USER</a>
 

 

