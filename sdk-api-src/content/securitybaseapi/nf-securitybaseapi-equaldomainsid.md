---
UID: NF:securitybaseapi.EqualDomainSid
title: EqualDomainSid function
author: windows-sdk-content
description: Determines whether two SIDs are from the same domain.
old-location: security\equaldomainsid.htm
old-project: secauthz
ms.assetid: a7eea3bd-33e0-427c-b023-07851c192eb2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EqualDomainSid, EqualDomainSid function [Security], _win32_equaldomainsid, security.equaldomainsid, securitybaseapi/EqualDomainSid
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
 - EqualDomainSid
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# EqualDomainSid function


## -description


The <b>EqualDomainSid</b> function determines whether two SIDs are from the same domain.


## -parameters




### -param pSid1 [in]

A pointer to one of the two SIDs to compare. This SID must be either an account domain SID or a BUILTIN SID.


### -param pSid2 [in]

A pointer to one of the two SIDs to compare. This SID must be either an account domain SID or a BUILTIN SID.


### -param pfEqual [out]

A pointer to a BOOL that <b>EqualDomainSid</b> sets to <b>TRUE</b> if the domains of the two SIDs are equal or <b>FALSE</b> if they are not equal. This value cannot be <b>NULL</b>.


## -returns



If both SIDs are  account domain SIDs and/or BUILTIN SIDs, the return value is nonzero. In addition, *<i>pfEqual</i> is set to <b>TRUE</b> if the domains of the two SIDs are equal; otherwise  *<i>pfEqual</i> is set to <b>FALSE</b>.

If one or more of the SIDS is neither an account domain SID nor a BUILTIN SID, then the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. <b>GetLastError</b> returns ERROR_NON_DOMAIN_SID if either SID is not an account domain SID or BUILTIN SID.




## -see-also




<a href="https://msdn.microsoft.com/ef41de63-4ab5-40c6-8b16-b960e1308b5b">EqualPrefixSid</a>



<a href="https://msdn.microsoft.com/08420df3-f6e6-462e-a2e6-d2a7a90be8ed">EqualSid</a>
 

 

