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
f1_keywords: 
 - "ntsecapi/LsaDeleteTrustedDomain"
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


The <b>LsaDeleteTrustedDomain</b> function removes a trusted domain from the list of trusted domains for a system and deletes the associated <a href="https://docs.microsoft.com/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://docs.microsoft.com/windows/desktop/SecMgmt/policy-object">Policy</a> object. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.


### -param TrustedDomainSid [in]

Pointer to the SID of the trusted domain to be removed.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a>
 

 

