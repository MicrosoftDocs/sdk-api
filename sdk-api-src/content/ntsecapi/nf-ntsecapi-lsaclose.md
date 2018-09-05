---
UID: NF:ntsecapi.LsaClose
title: LsaClose function
author: windows-sdk-content
description: The LsaClose function closes a handle to a Policy or TrustedDomain object.
old-location: security\lsaclose.htm
old-project: SecMgmt
ms.assetid: 6283b1da-4ec3-48e1-91f6-321c6390befe
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LsaClose, LsaClose function [Security], _lsa_lsaclose, ntsecapi/LsaClose, security.lsaclose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.redist: 
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaClose
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# LsaClose function


## -description


The <b>LsaClose</b> function closes a handle to a Policy or <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object.


## -parameters




### -param ObjectHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object returned by the 
<a href="https://msdn.microsoft.com/361bc962-1e97-4606-a835-cbce37692c55">LsaOpenPolicy</a> function or to a <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object returned by the 
<a href="https://msdn.microsoft.com/6c55f8b4-d8a2-48e3-8074-b3ca22ce487a">LsaOpenTrustedDomainByName</a> function. Following the completion of this call, the handle is no longer valid.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/361bc962-1e97-4606-a835-cbce37692c55">LsaOpenPolicy</a>
 

 

