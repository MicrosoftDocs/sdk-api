---
UID: NF:ntsecapi.LsaDeleteTrustedDomain
title: LsaDeleteTrustedDomain function (ntsecapi.h)
author: windows-sdk-content
description: The LsaDeleteTrustedDomain function removes a trusted domain from the list of trusted domains for a system and deletes the associated TrustedDomain object.
old-location: security\lsadeletetrusteddomain.htm
tech.root: SecMgmt
ms.assetid: 4a7afa28-1786-4a58-a955-d2d8b12e62e4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LsaDeleteTrustedDomain, LsaDeleteTrustedDomain function [Security], _lsa_lsadeletetrusteddomain, ntsecapi/LsaDeleteTrustedDomain, security.lsadeletetrusteddomain
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
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
api_name:
 - LsaDeleteTrustedDomain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LsaDeleteTrustedDomain function


## -description


The <b>LsaDeleteTrustedDomain</b> function removes a trusted domain from the list of trusted domains for a system and deletes the associated <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param TrustedDomainSid [in]

Pointer to the SID of the trusted domain to be removed.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/ms721859(v=VS.85).aspx">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a>
 

 

