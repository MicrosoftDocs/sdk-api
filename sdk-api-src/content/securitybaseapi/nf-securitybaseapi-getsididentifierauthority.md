---
UID: NF:securitybaseapi.GetSidIdentifierAuthority
title: GetSidIdentifierAuthority function
author: windows-sdk-content
description: Returns a pointer to the SID_IDENTIFIER_AUTHORITY structure in a specified security identifier (SID).
old-location: security\getsididentifierauthority.htm
tech.root: SecAuthZ
ms.assetid: 67a06e7b-775f-424c-ab36-0fc9b93b801a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetSidIdentifierAuthority, GetSidIdentifierAuthority function [Security], _win32_getsididentifierauthority, security.getsididentifierauthority, securitybaseapi/GetSidIdentifierAuthority
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
 - GetSidIdentifierAuthority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetSidIdentifierAuthority
: 
---

# GetSidIdentifierAuthority function


## -description


The <b>GetSidIdentifierAuthority</b> function returns a pointer to the 
<a href="https://msdn.microsoft.com/450a6d2d-d2e4-4098-90af-a8024ddcfcb5">SID_IDENTIFIER_AUTHORITY</a> structure in a specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


## -parameters




### -param pSid [in]

A pointer to the 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure for which a pointer to the 
<a href="https://msdn.microsoft.com/450a6d2d-d2e4-4098-90af-a8024ddcfcb5">SID_IDENTIFIER_AUTHORITY</a> structure is returned.

This function does not handle <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structures that are not valid. Call the <a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a> function to verify that the <b>SID</b> structure is valid before you call this function.


## -returns



If the function succeeds, the return value is a pointer to the <a href="https://msdn.microsoft.com/450a6d2d-d2e4-4098-90af-a8024ddcfcb5">SID_IDENTIFIER_AUTHORITY</a> structure for the specified 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure.

If the function fails, the return value is undefined. The function fails if the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure pointed to by the <i>pSid</i> parameter is not valid. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



This function uses a 32-bit RID value. For applications that require a larger RID value, use 
<a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a> and related functions.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a>



<a href="https://msdn.microsoft.com/0acaa804-494c-4d69-b1f7-8d167b494761">GetLengthSid</a>



<a href="https://msdn.microsoft.com/a481fb4f-20bd-4f44-a3d5-d8b8d6228339">GetSidLengthRequired</a>



<a href="https://msdn.microsoft.com/3a2d07f3-f1da-477d-b93f-525e3459dc61">GetSidSubAuthority</a>



<a href="https://msdn.microsoft.com/ca81fb91-f5a1-4dc6-83ec-eadb62a37805">GetSidSubAuthorityCount</a>



<a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/450a6d2d-d2e4-4098-90af-a8024ddcfcb5">SID_IDENTIFIER_AUTHORITY</a>
 

 

