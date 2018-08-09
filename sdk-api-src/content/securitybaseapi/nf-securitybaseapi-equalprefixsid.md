---
UID: NF:securitybaseapi.EqualPrefixSid
title: EqualPrefixSid function
author: windows-sdk-content
description: Tests two security-identifier (SID) prefix values for equality. A SID prefix is the entire SID except for the last subauthority value.
old-location: security\equalprefixsid.htm
old-project: secauthz
ms.assetid: ef41de63-4ab5-40c6-8b16-b960e1308b5b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EqualPrefixSid, EqualPrefixSid function [Security], _win32_equalprefixsid, security.equalprefixsid, securitybaseapi/EqualPrefixSid
ms.prod: windows
ms.technology: windows-sdk
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
 - EqualPrefixSid
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# EqualPrefixSid function


## -description


The <b>EqualPrefixSid</b> function tests two <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security-identifier</a> (SID) prefix values for equality. A SID prefix is the entire SID except for the last subauthority value.


## -parameters




### -param pSid1 [in]

A pointer to the first 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure to compare. This structure is assumed to be valid.


### -param pSid2 [in]

A pointer to the second <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure to compare. This structure is assumed to be valid.


## -returns



If the SID prefixes are equal, the return value is nonzero.

If the SID prefixes are not equal, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>EqualPrefixSid</b> function enables a server application in one domain to verify an attempt by a user to log on to another domain. For example, if a user attempts to log on to RemoteDomain from a workstation in LocalDomain, the server for LocalDomain can request the SIDs for the user and the user's groups from RemoteDomain. The domain controller for RemoteDomain responds with the relevant SIDs.

All SIDs for a specified domain have the same prefix. When the server receives the user's SIDs, the server can call the <b>EqualPrefixSid</b> function for each SID, comparing the user or group SID against the SID for RemoteDomain. If any of the SID prefixes are not equal, the server refuses the logon attempt.

It is advisable to modify the SID for a domain before comparing it with a group or user SID. If the SID for RemoteDomain is S-1–1234–8, each group or user SID for that domain has S-1–1234–8 as its prefix. To compare the SIDs by using the <b>EqualPrefixSid</b> function, an application copies the domain SID and adds any subauthority (<a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RID</a>) value to the copy, thereby creating a SID in the form S-1–1234–8–0. The application then uses the modified domain SID as a template against which the group and user SIDs are compared.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/2d7c182e-cdf8-4604-97bf-468bb4bd9232">CopySid</a>



<a href="https://msdn.microsoft.com/08420df3-f6e6-462e-a2e6-d2a7a90be8ed">EqualSid</a>



<a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

