---
UID: NF:securitybaseapi.IsValidSid
title: IsValidSid function
author: windows-sdk-content
description: Validates a security identifier (SID) by verifying that the revision number is within a known range, and that the number of subauthorities is less than the maximum.
old-location: security\isvalidsid.htm
tech.root: SecAuthZ
ms.assetid: 0fb08512-90a1-4a5c-9b4c-121bf7701bba
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IsValidSid, IsValidSid function [Security], _win32_isvalidsid, security.isvalidsid, securitybaseapi/IsValidSid
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
 - IsValidSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsValidSid function


## -description


The <b>IsValidSid</b> function validates a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) by verifying that the revision number is within a known range, and that the number of subauthorities is less than the maximum.


## -parameters




### -param pSid [in]

A pointer to the 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure to validate. This parameter cannot be <b>NULL</b>.


## -returns



If the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure is valid, the return value is nonzero.

If the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure is not valid, the return value is zero. There is no extended error information for this function; do not call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <i>pSid</i> is <b>NULL</b>, the application will fail with an access violation.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/0acaa804-494c-4d69-b1f7-8d167b494761">GetLengthSid</a>



<a href="https://msdn.microsoft.com/67a06e7b-775f-424c-ab36-0fc9b93b801a">GetSidIdentifierAuthority</a>



<a href="https://msdn.microsoft.com/a481fb4f-20bd-4f44-a3d5-d8b8d6228339">GetSidLengthRequired</a>



<a href="https://msdn.microsoft.com/3a2d07f3-f1da-477d-b93f-525e3459dc61">GetSidSubAuthority</a>



<a href="https://msdn.microsoft.com/ca81fb91-f5a1-4dc6-83ec-eadb62a37805">GetSidSubAuthorityCount</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>
 

 

