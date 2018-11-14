---
UID: NF:securitybaseapi.IsTokenRestricted
title: IsTokenRestricted function
author: windows-sdk-content
description: Indicates whether a token contains a list of restricted security identifiers (SIDs).
old-location: security\istokenrestricted.htm
tech.root: secauthz
ms.assetid: eaa63bb9-3084-4246-b2ab-f913bb7348fb
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: IsTokenRestricted, IsTokenRestricted function [Security], _win32_istokenrestricted, security.istokenrestricted, securitybaseapi/IsTokenRestricted
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
 - IsTokenRestricted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IsTokenRestricted
: 
---

# IsTokenRestricted function


## -description


The <b>IsTokenRestricted</b> function indicates whether a token contains a list of restricted <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs).


## -parameters




### -param TokenHandle [in]

A handle to an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> to test.


## -returns



If the token contains a list of restricting SIDs, the return value is nonzero.

If the token does not contain a list of restricting SIDs, the return value is zero.

If an error occurs, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a> function can restrict a token by disabling SIDs, deleting privileges, and specifying a list of restricting SIDs. The <b>IsTokenRestricted</b> function checks only for the list of restricting SIDs. If a token does not have any restricting SIDs, <b>IsTokenRestricted</b> returns <b>FALSE</b>, even though the token was created by a call to <b>CreateRestrictedToken</b>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>
 

 

