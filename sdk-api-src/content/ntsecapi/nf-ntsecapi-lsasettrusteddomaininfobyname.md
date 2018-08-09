---
UID: NF:ntsecapi.LsaSetTrustedDomainInfoByName
title: LsaSetTrustedDomainInfoByName function
author: windows-sdk-content
description: The LsaSetTrustedDomainInfoByName function sets values for a TrustedDomain object.
old-location: security\lsasettrusteddomaininfobyname.htm
old-project: secmgmt
ms.assetid: 263e1025-1010-463d-8bc7-cdf916ce9872
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LsaSetTrustedDomainInfoByName, LsaSetTrustedDomainInfoByName function [Security], TrustedDomainAuthInformation, TrustedDomainFullInformation, TrustedDomainInformationEx, TrustedPosixInformation, _lsa_lsasettrusteddomaininfobyname, ntsecapi/LsaSetTrustedDomainInfoByName, security.lsasettrusteddomaininfobyname
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - LsaSetTrustedDomainInfoByName
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# LsaSetTrustedDomainInfoByName function


## -description


The <b>LsaSetTrustedDomainInfoByName</b> function sets values for a 
<a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> of the trusted domain object determines whether the caller's changes are accepted. For information about policy object handles, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param TrustedDomainName [in]

Name of the trusted domain to set values for. This can either be the domain name or the flat name.


### -param InformationClass [in]

Specifies the type of information to set. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TrustedPosixInformation"></a><a id="trustedposixinformation"></a><a id="TRUSTEDPOSIXINFORMATION"></a><dl>
<dt><b>TrustedPosixInformation</b></dt>
</dl>
</td>
<td width="60%">
Posix offset of the trusted domain.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainInformationEx"></a><a id="trusteddomaininformationex"></a><a id="TRUSTEDDOMAININFORMATIONEX"></a><dl>
<dt><b>TrustedDomainInformationEx</b></dt>
</dl>
</td>
<td width="60%">
Extended trust information, including the basic information and DNS domain name, and attributes about the trust.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainAuthInformation"></a><a id="trusteddomainauthinformation"></a><a id="TRUSTEDDOMAINAUTHINFORMATION"></a><dl>
<dt><b>TrustedDomainAuthInformation</b></dt>
</dl>
</td>
<td width="60%">
Authentication information for the trust, including authentication information for both the inbound and outbound side of the trust (if it exists).

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainFullInformation"></a><a id="trusteddomainfullinformation"></a><a id="TRUSTEDDOMAINFULLINFORMATION"></a><dl>
<dt><b>TrustedDomainFullInformation</b></dt>
</dl>
</td>
<td width="60%">
Full information, including the Posix offset and the authentication information.

</td>
</tr>
</table>
 


### -param Buffer [in]

Pointer to a structure that contains the information to set. The type of structure depends on the value of the <i>InformationClass</i> parameter.
					


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
the "LSA Policy Function Return Values" section of <a href="management_return_values.htm">Security Management Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/d33d6cee-bd8b-49f4-8e65-07cdc65bec7c">LsaQueryTrustedDomainInfoByName</a>



<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>
 

 

