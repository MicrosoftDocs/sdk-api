---
UID: NF:securitybaseapi.GetWindowsAccountDomainSid
title: GetWindowsAccountDomainSid function
author: windows-sdk-content
description: Receives a security identifier (SID) and returns a SID representing the domain of that SID.
old-location: security\getwindowsaccountdomainsid.htm
tech.root: secauthz
ms.assetid: ee2ba1b4-1bef-4d79-bb18-512705e2c378
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetWindowsAccountDomainSid, GetWindowsAccountDomainSid function [Security], _win32_getwindowsaccountdomainsid, security.getwindowsaccountdomainsid, securitybaseapi/GetWindowsAccountDomainSid
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - GetWindowsAccountDomainSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetWindowsAccountDomainSid function


## -description


The <b>GetWindowsAccountDomainSid</b> function receives a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) and returns a SID representing the domain of that SID.


## -parameters




### -param pSid [in]

A pointer to the SID to examine.


### -param pDomainSid [out, optional]

Pointer that <b>GetWindowsAccountDomainSid</b> fills with a pointer to a SID representing the domain.


### -param cbDomainSid [in, out]

A pointer to a <b>DWORD</b> that <b>GetWindowsAccountDomainSid</b> fills with the size of the domain SID, in bytes.


## -returns



Returns <b>TRUE</b> if successful.

Otherwise, returns <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



