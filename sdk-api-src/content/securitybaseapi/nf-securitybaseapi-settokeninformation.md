---
UID: NF:securitybaseapi.SetTokenInformation
title: SetTokenInformation function
author: windows-sdk-content
description: Sets various types of information for a specified access token.
old-location: security\settokeninformation.htm
old-project: secauthz
ms.assetid: cdb8af74-540d-4059-ac64-6243f6aabaa6
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: SetTokenInformation, SetTokenInformation function [Security], _win32_settokeninformation, security.settokeninformation, securitybaseapi/SetTokenInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
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
 - SetTokenInformation
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# SetTokenInformation function


## -description


The <b>SetTokenInformation</b> function sets various types of information for a specified <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>. The information that this function sets replaces existing information. The calling process must have appropriate access rights to set the information.


## -parameters




### -param TokenHandle [in]

A handle to the access token for which information is to be set.


### -param TokenInformationClass [in]

A value from the 
<a href="https://msdn.microsoft.com/cb606665-1266-4e71-a145-9b04bf157cdc">TOKEN_INFORMATION_CLASS</a> enumerated type that identifies the type of information the function sets. The valid values from <b>TOKEN_INFORMATION_CLASS</b> are described in the <i>TokenInformation</i> parameter.


### -param TokenInformation [in]

A pointer to a buffer that contains the information set in the access token. The structure of this buffer depends on the type of information specified by the <i>TokenInformationClass</i> parameter.


### -param TokenInformationLength [in]

Specifies the length, in bytes, of the buffer pointed to by <i>TokenInformation</i>.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To set privilege information, an application can call the <a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> function. To set a token's groups, an application can call the <a href="https://msdn.microsoft.com/839c4b58-4c61-4f72-8337-1e3dfa267ee5">AdjustTokenGroups</a> function.

Token-type information can be set only when an access token is created.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/839c4b58-4c61-4f72-8337-1e3dfa267ee5">AdjustTokenGroups</a>



<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>



<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a>



<a href="https://msdn.microsoft.com/29fb738f-1ecd-4b72-9aea-64698cd74c12">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/cb606665-1266-4e71-a145-9b04bf157cdc">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/85617d56-ad46-40a3-a335-121f3c8edcc3">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/d23ebe6c-36a3-434a-a0fa-fcdf50dd19a0">TOKEN_PRIMARY_GROUP</a>
 

 

