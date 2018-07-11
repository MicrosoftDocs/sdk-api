---
UID: NF:securitybaseapi.GetSidLengthRequired
title: GetSidLengthRequired function
author: windows-sdk-content
description: Returns the length, in bytes, of the buffer required to store a SID with a specified number of subauthorities.
old-location: security\getsidlengthrequired.htm
old-project: secauthz
ms.assetid: a481fb4f-20bd-4f44-a3d5-d8b8d6228339
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: GetSidLengthRequired, GetSidLengthRequired function [Security], _win32_getsidlengthrequired, security.getsidlengthrequired, securitybaseapi/GetSidLengthRequired
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
 - GetSidLengthRequired
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# GetSidLengthRequired function


## -description


The <b>GetSidLengthRequired</b> function returns the length, in bytes, of the buffer required to store a SID with a specified number of subauthorities.


## -parameters




### -param nSubAuthorityCount [in]

Specifies the number of subauthorities to be stored in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure.


## -returns



The return value is the length, in bytes, of the buffer required to store the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure. This function cannot fail.




## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure specified in <i>nSubAuthorityCount</i> uses a 32-bit RID value. For applications that require longer RID values, use 
<a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a> and related functions.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/fcdff2f8-7f43-4c0f-b548-4914b1991937">AllocateAndInitializeSid</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a>



<a href="https://msdn.microsoft.com/0acaa804-494c-4d69-b1f7-8d167b494761">GetLengthSid</a>



<a href="https://msdn.microsoft.com/67a06e7b-775f-424c-ab36-0fc9b93b801a">GetSidIdentifierAuthority</a>



<a href="https://msdn.microsoft.com/3a2d07f3-f1da-477d-b93f-525e3459dc61">GetSidSubAuthority</a>



<a href="https://msdn.microsoft.com/ca81fb91-f5a1-4dc6-83ec-eadb62a37805">GetSidSubAuthorityCount</a>



<a href="https://msdn.microsoft.com/b2d803a5-faaf-4066-ba2c-0442c71bb150">InitializeSid</a>



<a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

