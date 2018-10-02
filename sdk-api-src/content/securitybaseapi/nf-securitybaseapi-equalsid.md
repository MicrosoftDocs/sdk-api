---
UID: NF:securitybaseapi.EqualSid
title: EqualSid function
author: windows-sdk-content
description: Tests two security identifier (SID) values for equality. Two SIDs must match exactly to be considered equal.
old-location: security\equalsid.htm
tech.root: SecAuthZ
ms.assetid: 08420df3-f6e6-462e-a2e6-d2a7a90be8ed
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EqualSid, EqualSid function [Security], _win32_equalsid, security.equalsid, securitybaseapi/EqualSid
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
 - EqualSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EqualSid function


## -description


The <b>EqualSid</b> function tests two <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) values for equality. Two SIDs must match exactly to be considered equal.


## -parameters




### -param pSid1 [in]

A pointer to the first 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure to compare. This structure is assumed to be valid.


### -param pSid2 [in]

A pointer to the second <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure to compare. This structure is assumed to be valid.


## -returns



If the 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structures are equal, the return value is nonzero.

If the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structures are not equal, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If either <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure is not valid, the return value is undefined.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/ef41de63-4ab5-40c6-8b16-b960e1308b5b">EqualPrefixSid</a>



<a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>
 

 

