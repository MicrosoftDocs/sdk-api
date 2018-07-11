---
UID: NF:securitybaseapi.GetSidSubAuthority
title: GetSidSubAuthority function
author: windows-sdk-content
description: Returns a pointer to a specified subauthority in a security identifier (SID). The subauthority value is a relative identifier (RID).
old-location: security\getsidsubauthority.htm
old-project: secauthz
ms.assetid: 3a2d07f3-f1da-477d-b93f-525e3459dc61
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: GetSidSubAuthority, GetSidSubAuthority function [Security], _win32_getsidsubauthority, security.getsidsubauthority, securitybaseapi/GetSidSubAuthority
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
 - GetSidSubAuthority
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# GetSidSubAuthority function


## -description


The <b>GetSidSubAuthority</b> function returns a pointer to a specified subauthority in a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID). The subauthority value is a <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">relative identifier</a> (RID).


## -parameters




### -param pSid [in]

A pointer to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure from which a pointer to a subauthority is to be returned.

This function does not handle <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structures that are not valid. Call the <a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a> function to verify that the <b>SID</b> structure is valid before you call this function.


### -param nSubAuthority [in]

Specifies an index value identifying the subauthority array element whose address the function will return. The function performs no validation tests on this value. An application can call the <a href="https://msdn.microsoft.com/ca81fb91-f5a1-4dc6-83ec-eadb62a37805">GetSidSubAuthorityCount</a> function to discover the range of acceptable values.


## -returns



If the function succeeds, the return value is a pointer to the specified <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> subauthority. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the function fails, the return value is undefined. The function fails if the specified <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure is not valid or if the index value specified by the <i>nSubAuthority</i> parameter is out of bounds. 




## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure specified in <i>pSid</i> uses a 32-bit RID value. For applications that require longer RID values, use 
<a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a> and related functions.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a>



<a href="https://msdn.microsoft.com/0acaa804-494c-4d69-b1f7-8d167b494761">GetLengthSid</a>



<a href="https://msdn.microsoft.com/67a06e7b-775f-424c-ab36-0fc9b93b801a">GetSidIdentifierAuthority</a>



<a href="https://msdn.microsoft.com/a481fb4f-20bd-4f44-a3d5-d8b8d6228339">GetSidLengthRequired</a>



<a href="https://msdn.microsoft.com/ca81fb91-f5a1-4dc6-83ec-eadb62a37805">GetSidSubAuthorityCount</a>



<a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

