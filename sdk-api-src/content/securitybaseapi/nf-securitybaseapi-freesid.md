---
UID: NF:securitybaseapi.FreeSid
title: FreeSid function
author: windows-sdk-content
description: Frees a security identifier (SID) previously allocated by using the AllocateAndInitializeSid function.
old-location: security\freesid.htm
tech.root: SecAuthZ
ms.assetid: 1e2098d8-4d1f-4353-97c1-549021a5b3fd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FreeSid, FreeSid function [Security], _win32_freesid, security.freesid, securitybaseapi/FreeSid
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
 - FreeSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeSid function


## -description


The <b>FreeSid</b> function frees a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) previously allocated by using the 
<a href="https://msdn.microsoft.com/fcdff2f8-7f43-4c0f-b548-4914b1991937">AllocateAndInitializeSid</a> function.


## -parameters




### -param pSid [in]

A pointer to the 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure to free.


## -returns



If the function succeeds, the function returns <b>NULL</b>.

If the function fails, it returns a pointer to the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure represented by the <i>pSid</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/fcdff2f8-7f43-4c0f-b548-4914b1991937">AllocateAndInitializeSid</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>
 

 

